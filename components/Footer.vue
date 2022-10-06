<template>
  <v-app dark class="w-footer">
    <v-container fluid class="first" >
      <v-row class="mx-auto">
        <v-col  cols="5">
          <v-img class="logo" :src="foot" height="45" contain width="auto"></v-img>
          <p>Subscribe to our newsletter</p>
          <v-row> 
            <v-text-field label="Enter your email" filled rounded dense>
            </v-text-field>
            <v-btn x-large rounded color="primary">subscribe</v-btn>
        </v-row>
        </v-col>
        <v-col cols="6">
          <v-container class="lis">
            <v-row>
              <v-col cols="12" sm="6" md="4">
                <div
                  class="footer-content"
                  v-for="(product, i) in footer.products"
                  :key="i"
                  :to="product.link"
                >
                  {{ product.name }}
                </div>
              </v-col>
              <v-col cols="4">
                <div
                  class="footer-content"
                  v-for="(product, i) in footer.aboutUs"
                  :key="i"
                  :to="product.link"
                >
                  {{ product.name }}
                </div>
              </v-col>
              <v-col cols="4">
                <div
                  class="footer-content"
                  v-for="(product, i) in footer.services"
                  :key="i"
                  :to="product.link"
                >
                  {{ product.name }}
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
        <v-col cols="1">
        <v-btn
                class="buttons"
                plain
                fab
                icon
                block
                v-for="(social, i) in socialLinks"
                :key="i"
                :to="social.link"
              >
                <v-icon>{{ social.icon }}</v-icon>
              </v-btn> </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  components: {},
  data: () => ({
    foot: require("@/assets/imgs/logo.png"),
    footer: {
      products: [
        { name: "Headphone", link: "/" },
        { name: "Earbuds", link: "/" },
        { name: "Speakers", link: "/" },
        { name: "Accessories", link: "/" },
      ],
      aboutUs: [
        { name: "About us", link: "/" },
        { name: "Contact", link: "/" },
        { name: "Privacy Police", link: "/" },
        { name: "Terms Of Use", link: "/" },
      ],
      services: [
        { name: "Order Status", link: "/" },
        { name: "Payment Methods", link: "/" },
        { name: "Shipping Delivery", link: "/" },
        { name: "FAQ", link: "/" },
      ],
    },
        socialLinks: [
      {
        icon: "mdi-instagram",
        link: "/",
      },
      {
        icon: "mdi-twitter",
        link: "/",
      },
      {
        icon: "mdi-facebook",
        link: "/",
      },
    ],
  }),
};
</script>

<style scoped>
.first{
  top: 50rem;
}
.buttons{
 top: 95px;
}
.logo{
    margin-bottom: 50px;
    top: 2rem;
    right: 11rem;
}
.footer-content {
  margin-bottom: 15px;
  color: #c3bebe;
}
.lis {
  margin-top: 15%;
  right: 90rem;
}
.w-footer {
  height: 500px;
}
.foot {
  left: 5%;
  margin-top: 10%;
}
p {
  color: #464646;
  font-family: 'roboto', sans-serif;
  margin-bottom: 10%;
  font-weight: 500;
  margin-left: 2.5rem;
}

.v-text-field{
      width: 340px !important;
      margin-left: 2.5rem;
      margin-right: 4rem;
}
.v-btn{
   right: 2rem;
}
</style>
