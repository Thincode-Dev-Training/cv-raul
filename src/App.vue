<template>
  <v-app>
    <v-card>
      <v-navigation-drawer
        app
        expand-on-hover
        permanent
        height="100%"
        width="300px"
        :src="require('@/assets/scott.jpg')"
      >
        <template v-slot:prepend>
          <v-list>
            <v-list-item>
              <v-list-item-avatar>
                <v-img :src="require('@/assets/me.jpg')"></v-img>
              </v-list-item-avatar>
            </v-list-item>

            <v-list-item
              link
              two-line
            >
              <v-list-item-content>
                <v-list-item-title class="title">Raul Alejandro Almanza Serrano</v-list-item-title>
                <v-list-item-subtitle>ra.almanzaserrano@gmail.com</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </template>

        <v-divider></v-divider>

        <v-list
          nav
        >
          <v-list-item color="#D8A31A" link to="/">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          <v-list-item color="#D8A31A" link to="/about">
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About me</v-list-item-title>
          </v-list-item>
          <v-list-item color="#D8A31A" link to="/resume">
            <v-list-item-icon>
              <v-icon>mdi-account-badge-horizontal-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Resume</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </v-card>

    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
};
</script>
