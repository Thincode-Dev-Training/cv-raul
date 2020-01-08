<template>
  <div class="bg">
    <v-container>
      <v-row style="height: 80px;">
        <v-col cols="12">
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-parallax :src="require('@/assets/scott.jpg')" >
            <v-row align="center" justify="center">
              <v-col class="text-center" cols="12">
                <h1>Raul Almanza</h1>
                <v-card max-width="100%" tilek>
                  <v-carousel cycle height="30px" width="100%" :show-arrows="false" hide-delimiters>
                    <v-carousel-item v-for="(desc, i) in descriptions" :key="i">
                      <v-sheet color="#B2EBF2" height="100%" >
                        <v-row class="fill-height" align="center" justify="center">
                          <span class="black--text">{{ desc }}</span>
                        </v-row>
                      </v-sheet>
                    </v-carousel-item>
                  </v-carousel>
              </v-card>
              </v-col>
            </v-row>
          </v-parallax>
        </v-col>
      </v-row>
      <v-row style="height: 80px;">
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
    data() {
      return {
        descriptions:['Web Developer', 'Problem Solver', 'Computer System Engeenier']
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Reem+Kufi&display=swap');

  h1, h2 {
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