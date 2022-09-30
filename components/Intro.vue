<template>
<div class="w-introduction">
  <v-list-item two-line>
      <v-list-item-content style="white-space: pre-line;">
        <v-list-item-title class="in">Popular products</v-list-item-title>
        <v-list-item-subtitle class="intro">An exclusive selections of our top selling products</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-btn
     plain
      color=#EF233C
      dark
    
    >
      View all new arrivals <v-icon small> mdi-arrow-right </v-icon>
    </v-btn>

 </div>
</template>
<script>
  export default {
    data: () => ({
      
    }),

  }
</script>
<style scoped>
.intro{
  font-family: 'Roboto', sans-serif;
font-size: 1.2rem;
font-weight: 400;
  white-space: normal;
  display:inline-block;
  word-wrap: break-word;
  margin-bottom: 50px;
}
.in{
  font-family: 'Roboto' sans-serif;
  font-size: 2.5rem;
  font-weight: 500;
  color: #000;
  margin-bottom: 50px;
}
.w-introduction{
  align-self: auto;
}
</style>
