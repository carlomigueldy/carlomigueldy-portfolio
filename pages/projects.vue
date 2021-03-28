<template>
  <div>
    <v-btn @click="$router.back()" text>Back</v-btn>
    
    <v-row class="py-5" v-for="item in 10" :key="item">
      <v-col cols="12" xs="12" sm="12" md="7" lg="7" xl="7">
        <h1>Title</h1>
        <p class="text-truncate">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo
          inventore quas aliquam magni expedita, ut, cupiditate a delectus,
          ducimus maiores ipsum voluptatum ea rem corporis nisi quis voluptatem
          quibusdam at.
        </p>
        <p>06-14-2020</p>
      </v-col>
      <v-col cols="12" xs="12" sm="12" md="5" lg="5" xl="5">
        <v-img
          class="rounded"
          src="https://townsquare.media/site/366/files/2019/06/GettyImages-965960520.jpg?w=980&q=75"
        ></v-img>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
export default {
  head: {
    title: "Carlo Miguel Dy | Projects"
  }
};
</script>

<style></style>
