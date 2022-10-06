<template>
  <div class="w-home">
    <v-card color="#191919" height="700px">
      <v-app>
        <v-container tile fluid fill-height>
          <v-row>
            <v-col cols="1">
              <v-btn
                class="bt"
                plain
                fab
                icon
                block
                v-for="(social, i) in socialLinks"
                :key="i"
                :to="social.link"
              >
                <v-icon>{{ social.icon }}</v-icon>
              </v-btn>
            </v-col>
            <div class="text">
              <v-col cols="6" align="left">
                <v-list-item max-height="50" two-line>
                  <v-list-item-content>
                    <v-list-item-title expand class="fo text-wrap font-weight-medium"
                      >Upbeat Wireless Headphones E60BT
                    </v-list-item-title>
                    <v-list-item-title class="pr">$219.78</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <div class="bn">
                <v-btn rounded color="red"> add to cart</v-btn>
              </div>
            </div>
            <v-col cols="4">
              <v-img class="w-img" :src="im"></v-img>
            </v-col>
            <v-col cols="1"
              ><v-timeline class="w-timeli">
                <v-timeline-item v-for="n in 3" :key="n" large>
                  <template v-slot:icon>
                    <div>{{ n }}</div>
                  </template>
                </v-timeline-item>
              </v-timeline>
              <div class="text-center">
                <v-pagination fab v-model="page" circle></v-pagination>
              </div>
            </v-col>
          </v-row>
          <div class="txt">
            <v-container>
              <v-row>
                <h1>Headphones</h1>
              </v-row>
            </v-container>
          </div>
        </v-container>
      </v-app>
    </v-card>
    <v-container fluid class="w-prod">
      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" class="w-prod"> <Intro /> </v-col>
        <v-col
          class="w-prod"
          cols="12"
          sm="6"
          md="4"
          lg="3"
          v-for="(product, idx) in products"
          :key="idx"
        >
          <Product :product="product"></Product>
        </v-col>
        <v-col cols="12" sm="6" md="4" lg="3"> <Todays /> </v-col>
      </v-row>
    </v-container>
    <v-container fill-height fluid>
      <v-row>
        <v-col cols="12">
          <v-img :src="pic">
            <v-container>
              <v-row>
                
                  <h1 class="image-text" align-center>Be ready fo feel next level sound</h1>
                  <p text-sub>Check out our latest Accessories</p>
               
                  <div class="shop-button">
                    <v-btn class="shop-button" rounded color="#EF233C" text-color="#F5F5F5"> Shop</v-btn>
                  </div>
                
              </v-row>
            </v-container>
          </v-img>
        </v-col>
      </v-row>
    </v-container>
    <v-container fill-height fluid>
      <v-row>
        <v-col cols="12">
          <v-img :src="picture"> </v-img>
        </v-col>
      </v-row>
    </v-container>
    <v-container fill-height fluid>
      <v-row>
        <v-col cols="12"> </v-col>
      </v-row>
    </v-container>
    <Footer />
  </div>
</template>
<script>
import Footer from "@/components/Footer";
import Todays from "@/components/Todays";
import Product from "@/components/Product";
import Intro from "@/components/Intro";
export default {
  componets: {
    Intro,
    Product,
    Todays,
    Footer,
  },
  data: () => ({
    im: require("@/assets/imgs/headphone.png"),
    pic: require("@/assets/imgs/pic.png"),
    picture: require("@/assets/imgs/pic2.PNG"),
    products: [
      {
        img: require("@/assets/imgs/hp1.PNG"),
        text: "Wireless Headphones 720",
        price: 106.58,
        discount: 0,
      },
      {
        img: require("@/assets/imgs/hp2.PNG"),
        text: "Wireless Headphones E45BT",
        price: 169.43,
        discount: 0,
      },
      {
        img: require("@/assets/imgs/hp3.PNG"),
        text: "Wireless Headphones E60BT",
        price: 219.78,
        discount: 0,
      },
      {
        img: require("@/assets/imgs/hp4.PNG"),
        text: "Wireless Headphones E900",
        price: 95.08,
        discount: 85.58,
      },
      {
        img: require("@/assets/imgs/hp5.PNG"),
        text: "Bluetooth Wireless Hearband",
        price: 106.58,
        discount: 52.39,
      },
      {
        img: require("@/assets/imgs/hp6.PNG"),
        text: "Wireless Headphones 720",
        price: 106.58,
        discount: 20.54,
      },
    ],

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
<style>
.shop-button {
  color: #ef233c;
}
.text-sub{
  text-decoration-color: #f5f5f5;
}
.image-text {

margin-left: 10rem;
  color: #f5f5f5;
  font-family: "Montserrat", sans-serif;
  word-wrap: break-word;
}
.w-prod {
  margin-top: 6%;
  border-style: none;
  width: 90rem;
}
.txtpr {
  font-size: 3rem;
  font-family: "Montserrat";
}
.text-center {
  position: absolute;
  left: 90%;
  top: 90%;
}
.bn {
  z-index: 4;
  margin-top: 20px;
  position: absolute;
  left: 32px;
}
.text {
  top: 12rem;
  width: 80rem;
  position: absolute;
  left: 10rem;
}
.ic {
  font-family: "Montserrat";
  font-size: 15px;
}
.w-timeli {
  position: absolute;
  left: 90%;
  top: 40%;
  color: white;
}
.w-img {
  position: absolute;
  width: 30rem;
  right: 11%;
  top: 15%;
  z-index: 2;
}
.fo {
  font-size: 60px;
  font-family: "roboto", sans-serif;
  top: 90px;
  z-index: 2;
  font-weight: 700;
  margin-bottom: 30px;
  word-spacing: 30px;
  line-height: 50px;
}
.w-logo {
  right: 6%;
  padding: 0%;
}
.pr {
  font-size: 25px;
  font-family: "Gotahm";
  z-index: 2;
  margin-top: 25px;
}

.ti {
  font-size: 55 px;
}

.bt {
  z-index: 2;
  top: 9.5rem;
  left: 2px;
}

.txt {
  font-size: 5.65rem;
  right: 4.5rem;
  position: relative;
  color: rgb(46, 46, 46);
  background-position: center;
  bottom: 30%;
  width: 95px;
}
</style>
