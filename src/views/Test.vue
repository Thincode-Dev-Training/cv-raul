<template>
  <div>
    <v-container class="pt-10">
      <v-data-table
        v-model="selected"
        :headers="headers"
        :items="desserts"
        :single-select="singleSelect"
        item-key="name"
        show-select
        class="elevation-1 test"
      >
        <template v-slot:top>
        </template>
      </v-data-table>
    </v-container>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        singleSelect: true,
        selected: [],
    desserts: [
        {
          name: 'Ruby Tutorial',
          calories: '6 meses',
          fat: 'Udemy',
          carbs: '02-04-2019',
          protein: 4.0,
          iron: '1%',
        },
        {
          name: '8 Beautiful Ruby on Rails Apps',
          calories: '1 mes',
          fat: 'Udemy',
          carbs: '01-08-2019',
          protein: 'N/A',
          iron: '1%',
        },
        {
          name: 'Rails with Active Record and Action Pack',
          calories: '3 meses',
          fat: 'Google',
          carbs: '15-10-2019',
          protein: 'N/A',
          iron: '1%',
        },
        {
          name: 'HTML, CSS, and Javascript for Web Developers',
          calories: '1 mes',
          fat: 'Google',
          carbs: '01-11-2019',
          protein: 4.0,
          iron: '1%',
        },
        {
          name: 'GraphQL',
          calories: '1 mes',
          fat: 'Coursera',
          carbs: '01-12-2019',
          protein: 4.0,
          iron: '1%',
        }
      ],
      headers: [
        {
          text: 'Curso',
          align: 'left',
          sortable: false,
          value: 'name',
        },
        { text: 'Duración', value: 'calories' },
        { text: 'Institución', value: 'fat' },
        { text: 'Fecha', value: 'carbs' }
      ],
      }
    },
  }
</script>

<style scoped>
  thead { background-color: #00f; }
</style>
