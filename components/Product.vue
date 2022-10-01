<template>
    <v-card flat class="mx-15 my-15" max-width="400">
    
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img height="300" :src="product.img">
     </v-img>
       
      <v-card-title class="text--black te" v-text="product.text"></v-card-title
    >
    <v-card-subtitle v-text="product.subtext"></v-card-subtitle>
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
};
</script>
<style scoped>
 .te{
  font-family: 'Montserrat' sans-serif;
  font-size: 15px;
  font-weight: 700;
 }
</style>