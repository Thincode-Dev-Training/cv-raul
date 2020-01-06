<template>
  <div class="bg">
    <v-container>
      <v-row style="height: 150px;">
        <v-col cols="12">
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-parallax :src="require('@/assets/scott.jpg')" >
            <v-row align="center" justify="center">
              <v-col class="text-center" cols="12">
                <h1>Raul Almanza</h1>
                <h2 style="color: #84A9C6;">Fullstack Developer</h2>
              </v-col>
            </v-row>
          </v-parallax>
        </v-col>
      </v-row>
      <v-row style="height: 150px;">
        <v-col cols="12">
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
  export default {
    name: 'home',
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Reem+Kufi&display=swap');

  h1 {
    font-family: 'Reem Kufi', sans-serif;
    color: #2B303A;
    font-weight: 100;
    font-size: 50px;
  }
  .bg {
    height: 100%;
    background-image: linear-gradient(to left bottom, #acecea, #abe3e9, #add9e5, #b0cfde, #b3c6d5);
  }
</style>