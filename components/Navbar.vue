<template>
  <header>
    <nuxt-link :src="logo" tag="img" to="/" class="logo"></nuxt-link>
    <nav>
      <ul class="nav_links">
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/catalog">catalog</nuxt-link></li>
        <li><nuxt-link to="/contact">Contact</nuxt-link></li>
        <li><nuxt-link to="/support">Support</nuxt-link></li>
      </ul>
    </nav>
    <a class="cta" href="#">
      <v-btn icon>
        <v-icon color="#f5f5f5">mdi-cart-outline</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="#f5f5f5">mdi-heart-outline</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="#f5f5f5">mdi-account-outline</v-icon>
      </v-btn>
    </a>
  </header>
</template>
<script>
export default {
  data: () => ({
    logo: require("@/assets/imgs/logo.png"),
  }),
};
</script>
<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  background-color: #0f0f0f;
}
.logo{
  right: 90%;
}
li,
a {
  font-family: "Montserrat", sans-serif;
  font-weight: 500;
  font-size: 16px;
  color: #f5f5f5;
  text-decoration: none;
}
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 4%;
}

.nav_links {
  list-style: none;
}
.nav_links li {
  display: inline-block;
  padding: 0px 20px;
}
.nav_links li a {
  transition: all 0.3s ease 0s;
}
.nav_links li a:hover {
  color: #ef233c;
}
</style>
