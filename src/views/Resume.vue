<template>
  <div class="bg">
    <v-container wrap>
      <v-row style="height: 70px;">
        <v-col cols="12">
        </v-col>
      </v-row>
      <v-row style="background: #33425F; padding-botton: 5px;" class="elevation-5">
        <v-col cols="12" md="6" >
          <v-chip label color="#F9F871" style="width: 100%" >
            <v-icon class="mr-5">mdi-school</v-icon>
            <h2>Education</h2>
          </v-chip>
          <v-timeline dense>
            <v-timeline-item large>
              <template v-slot:icon>
                <v-avatar>
                  <img :src="require('@/assets/ug.jpeg')">
                </v-avatar>
              </template>
              <v-card class="elevation-2">
                <v-card-title style="font-size: 15px;">UNIVERSIDAD DE GUANAJUATO - DICIS</v-card-title>
                <v-card-subtitle>COMPUTER SYSTEMS ENGINEER</v-card-subtitle>
                <v-card-text>Focused on Computer Vision, Data Mining and development for web MVC applications. Specialized on several programming languages such as C/C++/Python (for Computer Vision and Data Mining), RoR and Javascript.</v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-col>
        <v-col cols="12" md="6">
          <v-chip label color="#F9F871" style="width: 100%" >
            <v-icon class="mr-5">mdi-code-greater-than</v-icon>
            <h2>Coding skills</h2>
          </v-chip>
          <v-card class="elevation-2 mt-5">
            <v-card-text>
              <v-chip label color="#F9F871" class="mt-5" >
                <v-icon class="mr-3">mdi-script</v-icon>
                Programming languages
              </v-chip>
              <v-row v-for="(lang, index) in languages" :key="index">
                <v-col cols="3">
                  <h4>{{lang.name}}</h4>
                </v-col>
                <v-col cols="9">
                  <v-progress-linear
                    :buffer-value="100"
                    :striped="true"
                    :value="lang.value*20"
                    color="light-blue"
                    height="13px"
                  ></v-progress-linear>
                </v-col>
              </v-row>
              <v-chip label color="#F9F871" class="mt-5" >
                <v-icon class="mr-3">mdi-database</v-icon>
                Databases
              </v-chip>
              <v-row v-for="(db, index) in databases" :key="index">
                <v-col cols="3">
                  <h4>{{db.name}}</h4>
                </v-col>
                <v-col cols="9">
                  <v-progress-linear
                    :buffer-value="100"
                    :striped="true"
                    :value="db.value*20"
                    color="light-blue"
                    height="13px"
                  ></v-progress-linear>
                </v-col>
              </v-row>
              <v-chip label color="#F9F871" class="mt-5" >
                <v-icon class="mr-3">mdi-web</v-icon>
                Web Frameworks
              </v-chip>
              <v-row v-for="(fw, index) in frameworks" :key="index">
                <v-col cols="3">
                  <h4>{{fw.name}}</h4>
                </v-col>
                <v-col cols="9">
                  <v-progress-linear
                    :buffer-value="100"
                    :striped="true"
                    :value="fw.value*20"
                    color="light-blue"
                    height="13px"
                  ></v-progress-linear>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-row class="mt-10 elevation-5" style="background: #33425F;">
        <v-col cols="12">
          <v-chip label color="#F9F871" style="width: 100%" >
            <v-icon class="mr-5">mdi-briefcase</v-icon>
            <h2>Experience</h2>
          </v-chip>
        </v-col>
        <v-row>
          <v-col cols="12" md="6" v-for="(exp, index) in experiences" :key="index">
            <v-card class="elevation-2 mx-3">
              <v-list-item three-line>
                <v-list-item-content>
                  <div class="overline mb-4">{{exp.role}}</div>
                  <v-list-item-title class="headline mb-1">{{exp.name}}</v-list-item-title>
                  <v-list-item-subtitle>{{exp.time}}</v-list-item-subtitle>
                </v-list-item-content>

                <v-list-item-avatar tile size="80" color="white">
                  <v-img :src="require('@/assets/' + exp.image)"></v-img>
                </v-list-item-avatar>
              </v-list-item>
              <v-card-subtitle>{{exp.description}}</v-card-subtitle>
              <v-divider class="mx-5"></v-divider>

              <v-card-text>
                <v-subheader>Major Accomplishments</v-subheader>
                <ul>
                  <li v-for="(acc, i) in exp.accomplishments" :key="i">{{acc}}</li>
                </ul>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'resume',
  data() {
    return {
      value: 0,
      interval: 0,
      languages: [
        {name: 'Python', value: 4},
        {name: 'C/C++', value: 4},
        {name: 'Ruby', value: 5}
        ],
      databases: [
        {name: 'MySQL', value: 4},
        {name: 'PostgreSQL', value: 4}
        ],
      frameworks: [
        {name: 'Rails', value: 5},
        {name: 'Django', value: 3},
        {name: 'VueJS', value: 4},
        {name: 'Angular', value: 3}
        ],
      experiences:[
        {
          name: 'Thincode',
          image: 'thincode.png',
          role: 'Software Developer',
          time: 'July 2017 - Present',
          description:'Software development for banking systems using low-level programming languages for complex and high performance systems. Development of REST API for web applications using Ruby on Rails and PostgreSQL, Python with Django, all of those while working under Agile methodologies.',
          accomplishments: [
            'Modifications for international electronic payment systems',
            'Development of REST APIs for web applications',
            'Implementations of CI/CD on DevOps projects using Jenkins',
            'Cloud Computing using Amazon Web Services',
            'Angular for Front-End development of web applications',
            'Development of RESTful APIs using Django and SQL Databases for Banking Services.'
            ]
        },
        {
          name: 'CEMER SC',
          image: 'cemersc.png',
          role: 'Software Developer',
          time: 'August 2016 – February 2017',
          description:'Software development of an Android application and a SCADA system to measure and registration of data from photovoltaic equipment and solar panels.',
          accomplishments: [
            'Development of an Android application for orienting and installing solar panels.',
            'Development of a SCADA system for measuring and registering data from photovoltaic equipment, using python.'
            ]
        }
      ]
    }
  },
}
</script>

<style scoped>
  h2 {
     font-size: 30px;
  }
</style>