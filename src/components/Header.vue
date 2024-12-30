<template>
  <header>
    <div class="logo">Fishing Tackle Shop</div>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(0, 0, 0, 0.7);
    color: #fff;
    padding: 1rem 2rem;
}

header .logo {
    font-size: 1.5rem;
    font-weight: bold;
}

header nav ul {
    list-style: none;
    display: flex;
}

header nav ul li {
    margin-left: 1rem;
}

header nav ul li a {
    color: #fff;
    text-decoration: none;
}
</style>
