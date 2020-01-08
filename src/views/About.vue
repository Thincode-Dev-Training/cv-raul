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
        <v-col cols="12" md="3" align="center">
          <v-avatar size="200" class="pt-12">
            <v-img width="100%" class="elevation-6" :src="require('@/assets/me.jpg')"></v-img>
          </v-avatar>
        </v-col>
        <v-col cols="6" md="4">
          <h2>Hello there! i am Raul Almanza</h2>
          <v-divider></v-divider>
          <p class="mt-5">I am an enthusiastic and dedicated to my job person, I like web and mobile applications development. I want to apply my skills to develop quality software and continuously learn new tools and technologies.</p>
        </v-col>
        <v-col cols="6" md="5">
          <v-divider class="mt-7 mb-5"></v-divider>
          <p>
            <v-icon color="yellow" class="mr-2">mdi-cake-variant</v-icon>
            <u class="mr-5">Age:</u> {{age()}}
          </p>
          <p>
            <v-icon color="yellow" class="mr-2">mdi-map-marker-radius</v-icon>
            <u class="mr-5">Residence:</u> Valle de Santiago, Gto. México
          </p>
          <p>
            <v-icon color="yellow" class="mr-2">mdi-at</v-icon>
            <u class="mr-5">Email:</u> ra.almanzaserrano@gmail.com
          </p>
          <p>
            <v-icon color="yellow" class="mr-2">mdi-cellphone</v-icon>
            <u class="mr-5">Phone:</u> 4561146217
          </p>
          <v-row class="my-10">
            <h3 style="color: #F9F871;">Social media:</h3>
            <v-col cols="12">
              <v-btn icon outlined color="yellow" href="https://github.com/Ruli-AlSe" elevation="5">
                <v-icon>mdi-github-circle</v-icon>
              </v-btn>
              <v-btn icon outlined color="yellow" elevation="5" class="ml-3" href="https://www.facebook.com/AlejandroAlmanzaRully">
                <v-icon>mdi-facebook</v-icon>
              </v-btn>
              <v-btn icon outlined color="yellow" elevation="5" class="ml-3" href="https://www.linkedin.com/in/raul-alejandro-almanza-serrano">
                <v-icon>mdi-linkedin</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" md="6">
          <v-chip label color="#F9F871" style="width: 50%" >
            <h3>Languages</h3>
          </v-chip>
          <v-card class="mt-5">
            <v-card-text>
              <v-row v-for="(lang, index) in languages" :key="index">
                <v-col cols="3">
                  <h4>{{lang.name}}</h4>
                </v-col>
                <v-col cols="9">
                  <v-progress-linear
                    :buffer-value="100"
                    :striped="true"
                    :value="lang.value*20"
                    color="#8F6F9B"
                    height="13px"
                  ></v-progress-linear>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" md="6">
          <v-chip label color="#F9F871" style="width: 50%" >
            <h3>Soft skills</h3>
          </v-chip>
          <v-card class="mt-5">
            <v-card-text>
              <v-row>
                <v-col cols="3" v-for="(skill, index) in skills" :key="index">
                  <li><b>{{skill}}</b></li>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-row style="height: 100px;"></v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'about',
  data() {
    return {
      languages: [
        {name: 'Spanish', value: 5},
        {name: 'English', value: 4.3}
      ],
      skills: ['Teamwork', 'Commitment', 'Determination', 'Fast learner', 'Responsibility']
    }
  },
  methods: {
    age() {
      var date = Date(Date.now()).toString().split(' ')
      return date[3] - 1994
    }
  }
}
</script>

<style scoped>
  h2 {
    color: #FFFFFF;
    font-size: 25px;
  }
  u, p {
    color: #F9F871;
    font-size: 17px;
  }
</style>
