<template>
  <div>
    <v-row style="height: 100px;">
      <v-col cols="12">
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <v-parallax
          src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
        >
          <v-row
            align="center"
            justify="center"
          >
            <v-col class="text-center" cols="12">
              <h1>Raul Almanza</h1>
              <h2>Fullstack Developer</h2>
            </v-col>
          </v-row>
        </v-parallax>
      </v-col>
    </v-row>
    <v-row style="height: 100px;">
      <v-col cols="12">
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src
  export default {
    name: 'home',
  }
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css?family=Reem+Kufi&display=swap');

  h1 {
    font-family: 'Reem Kufi', sans-serif;
    color: #3A405A;
    font-weight: 100;
    font-size: 50px;
  }
</style>