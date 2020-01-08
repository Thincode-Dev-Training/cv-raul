<template>
  <div class="bg">
    <v-container wrap>
      <v-row>
        <v-col cols="12" align="center">
          <h1>About me</h1>
          <v-chip label outlined color="#33425F">
            <b>Programmer, enthusiastic guy, problem solver</b>
          </v-chip>
        </v-col>
      </v-row>
      <v-row style="background: #33425F;" class="mt-10">
        <v-col cols="12" md="4" align="center">
          <v-avatar size="200" class="pt-12">
            <v-img width="100%" class="elevation-6" :src="require('@/assets/me.jpg')"></v-img>
          </v-avatar>
        </v-col>
        <v-col cols="6" md="4">
          <h3>Hello there! i am Raul Almanza</h3>
          <v-divider></v-divider>
          <p class="mt-5">I am an enthusiastic and dedicated to my job person, I like web and mobile applications development. I want to apply my skills to develop quality software and continuously learn new tools and technologies.</p>
        </v-col>
        <v-col cols="6" md="4">
          <v-divider class="mt-7 mb-5"></v-divider>
          <p><u class="mr-5">Age:</u> {{age()}}</p>
          <p><u class="mr-5">Residence:</u> Irapuato, Gto. México</p>
          <p><u class="mr-5">Email:</u> raul.almanza@thincode.com</p>
          <p><u class="mr-5">Phone:</u> 456XXXXXXX</p>
          <h3>Social media:</h3>
          <v-row>
            <v-col cols="12">
              <v-btn icon outlined color="#DCE8E3" href="https://github.com/Ruli-AlSe" elevation="5">
                <v-icon>mdi-github-circle</v-icon>
              </v-btn>
              <v-btn icon outlined color="#DCE8E3" elevation="5" class="ml-3" href="https://www.facebook.com/AlejandroAlmanzaRully">
                <v-icon>mdi-facebook</v-icon>
              </v-btn>
              <v-btn icon outlined color="#DCE8E3" elevation="5" class="ml-3" href="https://www.linkedin.com/in/raul-alejandro-almanza-serrano-262727166/">
                <v-icon>mdi-linkedin</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'about',
  methods: {
    age() {
      var date = Date(Date.now()).toString().split(' ')
      return date[3] - 1994
    }
  }
}
</script>

<style scoped>
  h3, p{
    color: #FFFFFF
  }
</style>
