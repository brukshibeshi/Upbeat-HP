<template>
  <div class="deals">
    <v-img class="tod" :src="today"> </v-img>
    <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title class="today">Today's Deals</v-list-item-title>
        <v-list-item-subtitle class="sub"
          >Save money on the best Deals of the day</v-list-item-subtitle
        >
      </v-list-item-content>
    </v-list-item>
    <v-btn plain color="#EF233C" dark>
      View all new arrivals <v-icon small> mdi-arrow-right </v-icon>
    </v-btn>
  </div>
</template>
<script>
export default {
  data: () => ({
    today: require("@/assets/imgs/today.PNG"),
  }),
};
</script>

<style scoped>
.tod {
  width: 5rem;
  height: 5rem;
  margin-top: 5rem;
  left: 30%;
  margin-bottom: 50px;
}
.today {
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  font-size: 40px;
  left: 50%;
}
.sub {
  font-family: 'Montserrat';
  font-size: 15px;
  font-weight: 500;
  white-space: normal;
  display: inline-block;
  word-wrap: break-word;
  margin-bottom: 50px;
}
.deals {
  right: 70%;
}
</style>
