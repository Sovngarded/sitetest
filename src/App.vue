<template>
  <v-app style="background: #1C1D21;" >
    <v-main >
      <v-container >
        <v-layout row wrap align-content-center>
          <v-flex class="text-lg-center">
        <div>
        <h1 >
        Kibirev Artem
          </h1>
        </div>
        <div class="photo">
          <img src="@/pictures/1.jpg">
        </div>
            <v-expansion-panels>
            <v-expansion-panel>
              <v-expansion-panel-header color="#7E4E60">
                ПОСМОТРЕТЬ РАСПИСАНИЕ
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-data-table
                    :headers="headers"
                    :items="workthings"
                    :items-per-page="5"
                    class="elevation-1"
                ></v-data-table>
              </v-expansion-panel-content>
            </v-expansion-panel>
            </v-expansion-panels>


      </v-flex>
      </v-layout>
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
export default {
  name: 'App',
  components: {
  },
  data () {
    return {
      headers: [
        {
          text: 'Что делаю',
          align: 'center',
          sortable: false,
          value: 'name',
        },
        { text: 'Когда', value: 'when' },
        { text: 'Зачем', value: 'why' },

      ],
      workthings: [
        {
          name: 'Встаю',
          when:'10:00',
          why:'а смысла нет каждый день'
        },
        {
          name: 'Ем',
          when:'10:20',
          why:'вкусно поесть всегда надо'
        },
        {
          name: 'Еду в колледж на любимой 43 маршрутке',
          when:'10:40',
          why:'как всегда опаздываю маршрутчику не прикажешь'
        },
        {
          name: 'Впитываю информацию и жду обеда',
          when:'10:45',
          why:'ох когда же в столовку'
        },
        {
          name: 'Ем',
          when:'12:20',
          why:'ох как вкусно'
        },
        {
          name: 'Еду домой',
          when:'14:35',
          why:'Спасибо Клим Саныч. Потраченного времени жаль. Пятикратно переваренный кал.'
        }
      ],
    }
  },
}
</script>
<style>
img{
  width: 500px;
}
h1{
  font: italic small-caps bold 60px/2 cursive;
  color:#BB9BB0;
  text-shadow: 2px 2px 0px #ffffff, 5px 4px 0px rgba(0,0,0,0.15), 2px 2px 2px rgba(206,89,55,0);
}
</style>
