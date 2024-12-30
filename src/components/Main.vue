<template>
  <main>
    <!-- Home Section -->
    <section id="home" class="hero">
      <h1>Welcome to Fishing Tackle Shop</h1>
      <p>Your one-stop shop for all fishing gear! Explore our wide variety of fishing rods, reels, baits, and accessories.</p>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
      <h2>Our Products</h2>
      <p>We offer a wide range of fishing gear to suit your needs. Whether you're an experienced angler or just starting out, we have everything you need!</p>
      <div class="product-list">
        <div v-for="product in products" :key="product.id" class="product-item">
          <img :src="product.image" :alt="product.name" />
          <h3>{{ product.name }}</h3>
          <p>{{ product.description }}</p>
          <button class="buy-btn" @click="buyProduct(product)">Buy Now</button>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
      <h2>About Us</h2>
      <p>We are a passionate team dedicated to providing the best fishing gear to anglers all over the world. Our goal is to ensure that every fishing experience is enjoyable and successful.</p>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
      <h2>Contact Us</h2>
      <p>If you have any questions or would like to place an order, feel free to contact us:</p>
      <p>Email: <a href="mailto:Vincent Dua orang @gmail.com">Vincent Dua orang @gmail.com</a></p>
      <p>Phone: 082145862699</p>
    </section>x``
  </main>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Fishing Rod",
          description: "This high-quality fishing rod is designed for both beginners and pros.",
          image: "../src/img/JORAN.jpg",
        },
        {
          id: 2,
          name: "Fishing Reel",
          description: "Our fishing reels are smooth and reliable.",
          image: "../src/img/REEL.jpg",
        },
        {
          id: 3,
          name: "Bait",
          description: "We provide a selection of top-notch baits.",
          image: "../src/img/UMPAN.jpg",
        },
        {
          id: 4,
          name: "Fish Net",
          description: "This high-quality fish net is designed for efficient fish capture.",
          image: "../src/img/JARING_IKAN.jpg",
        },
      ],
    };
  },
  methods: {
    buyProduct(product) {
      alert(`You have selected: ${product.name}`);
    },
  },
};
</script>

<style scoped>
  body {
    font-family: "Arvo", serif;
    line-height: 1.6;
    background-size: cover;
    background-position: center;
}

.hero {
    text-align: center;
    padding: 5rem 2rem;
    background-image: url(../img/TEBING.jpg);
    background-size: cover;
    background-position: center;
    color: #fff;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.products {
    padding: 2rem;
    background-color: rgba(255, 255, 255, 0.9);
}

.products h2 {
    text-align: center;
    margin-bottom: 1rem;
}

.products p {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 1.1rem;
}

.product-list {
    display: flex;
    gap: 2rem;
    justify-content: center;
    flex-wrap: wrap;
}

.product-item {
    text-align: center;
    width: 300px;
}

.product-item img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;
}

.product-item img:hover {
    transform: scale(1.05);
}

.product-item h3 {
    font-size: 1.5rem;
    margin-top: 1rem;
    color: #333;
}

.product-item p {
    font-size: 1rem;
    color: #555;
    margin-top: 0.5rem;
}

.about,
.contact {
    padding: 2rem;
    text-align: center;
    background-color: #f4f4f4;
}
</style>
