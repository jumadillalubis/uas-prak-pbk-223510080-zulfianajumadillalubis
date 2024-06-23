<template>
    <nav class="navbar">
      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">WEATHER</router-link>
      </div>
      <div class="task-links">
        <div class="dropdown" @click="toggleDropdown">
          <div class="navbar-item">👩‍💻TUGAS DILLA ▼</div> <!-- Menambah panah ke bawah -->
          <div class="dropdown-menu" :class="{ 'is-active': isDropdownActive }">
            <a href="https://tugas1-pbk-223510080.vercel.app/" class="navbar-item" target="_blank">TUGAS 1</a>
            <a href="https://dillaatugas2-prakpbk-dv40d21wr.vercel.app/" class="navbar-item" target="_blank">TUGAS 2</a>
            <a href="https://dilla-tugas3-9uatdek5d-zulfiana-jumadilla-lubis-projects.vercel.app/" class="navbar-item" target="_blank">TUGAS 3</a>
            <a href="https://dillat4-7f1yjr29y-zulfiana-jumadilla-lubis-projects.vercel.app/" class="navbar-item" target="_blank">TUGAS 4</a>
            <a href="https://t5-prak-pbk-zulfiana-jumadilla-lubis-223510080.vercel.app/" class="navbar-item" target="_blank">TUGAS 5</a>
            <a href="https://dillatugas6.vercel.app/" class="navbar-item" target="_blank">TUGAS 6</a>
            <a href="https://t7-dilla.vercel.app/" class="navbar-item" target="_blank">TUGAS 7</a>
          </div>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar',
    data() {
      return {
        isDropdownActive: false
      };
    },
    methods: {
      toggleDropdown() {
        this.isDropdownActive = !this.isDropdownActive;
      }
    }
  };
  </script>
  
  <style scoped>
  .navbar {
    background-color: #0d0f11d4;
    color: #fff;
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .navbar-brand {
    display: flex;
    align-items: center;
  }
  
  .navbar-item {
    color: #fff;
    text-decoration: none;
    margin: 0 10px;
    padding: 10px;
    border-radius: 5px;
    transition: background-color 0.3s, color 0.3s;
    font-size: 18px; /* Menambah ukuran font */
  }
  
  .navbar-item:hover {
    background-color: #1177e4;
  }
  
  .task-links {
    display: flex;
    align-items: center;
  }
  
  .dropdown {
    position: relative;
    cursor: pointer; /* Menambahkan cursor pointer untuk menunjukkan klik-able */
  }
  
  .dropdown-menu {
    display: none;
    position: absolute;
    top: calc(100% + 10px); /* Menyesuaikan jarak dari navbar */
    left: 50%;
    transform: translateX(-50%);
    background-color: #1b1e1d;
    border-radius: 10px;
    padding: 10px 0; /* Mengurangi padding untuk konten lebih ringan */
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    z-index: 1000;
    width: 200px;
    opacity: 0; /* Mengatur opacity untuk animasi */
    pointer-events: none; /* Menonaktifkan event di luar tampilan */
    transition: opacity 0.3s ease; /* Animasi opacity */
  }
  
  .dropdown-menu.is-active {
    display: block;
    opacity: 1; /* Menampilkan dropdown */
    pointer-events: auto; /* Mengaktifkan event kembali */
  }
  
  .dropdown-menu .navbar-item {
    display: block;
    width: 100%;
    padding: 10px 20px; /* Menyesuaikan padding untuk konten */
    font-size: 16px; /* Menurunkan ukuran font untuk konten dropdown */
  }
  
  .dropdown-menu .navbar-item:hover {
    background-color: #0056b3;
  }
  
  .navbar-item.active {
    background-color: #0056b3;
  }
  </style>
  