<template>
  <div>
    <v-main>
    <Navbar />
      <nuxt />
    </v-main>  
  </div>
</template>
<script>
import Navbar from "@/components/Navbar";
export default {
  components: {
    Navbar,   
  },
};
</script>
<style scoped></style>
