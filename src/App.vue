<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<style>
/* General button styles */
.buy-btn {
  background-color: #4caf50; /* Warna hijau */
  color: white; /* Warna teks putih */
  padding: 12px 24px; /* Padding untuk ukuran tombol */
  text-align: center; /* Teks rata tengah */
  text-decoration: none; /* Menghapus underline */
  display: inline-block; /* Agar tombol bisa sejajar dengan elemen lainnya */
  font-size: 16px; /* Ukuran font */
  border: none; /* Menghilangkan border default */
  cursor: pointer; /* Menunjukkan bahwa tombol dapat diklik */
  border-radius: 5px; /* Sudut melengkung */
  transition: background-color 0.3s ease; /* Animasi perubahan warna */
  margin-top: 10px; /* Menambahkan jarak atas tombol */
}

.buy-btn:hover {
  background-color: #45a049;
}

html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    overflow-x: hidden; /* Untuk mencegah elemen melampaui viewport */
    background-image: url(../src/img/BACKGROUND.jpg);
    background-size: cover;
}
</style>
