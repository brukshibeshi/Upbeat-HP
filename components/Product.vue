<template>
  <v-card flat class="mx-15 my-15" max-width="400">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>
    <v-img class="product-img" height="300" :src="product.img"> </v-img>
    <v-chip  color="#EF233C" class="discount-chips" v-show="hasDiscount" :ripple="false">
      15% Off
    </v-chip>
    <div class="text--black te" v-text="product.text"></div>
    <div>
      <span :class="{ 'discount': hasDiscount}">
        {{ product.price }}</span
      >
      <span  v-show="hasDiscount" class="discount-text">{{ product.discount }} </span>
    </div>
  </v-card>
</template>
<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
  data: () => ({}),

  methods: {},
  computed:{
    hasDiscount() {
      return this.product && this.product.discount > 0 
    }
  },
};
</script>
<style scoped>
.te {
  font-family: "Montserrat" sans-serif;
  font-size: 16px;
  font-weight: 700;
}
.discount {
  text-decoration: line-through;
}
.discount-text{
  margin-left: 2rem;
}
.discount-chips{
position: absolute;
top: 0px;
right: 15px;
width: 86px;
height: 35px;
color: #f3eaeb;
}
.product-img{
  position: relative;
}

</style>
