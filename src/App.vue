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
            <v-hover v-slot="{ hover }">
              <v-card
                  class="mx-auto"
                  color="grey lighten-4"
                  max-width="600"
              >
            <v-img :src="require('./pictures/1.jpg')" :aspect-ratio="16/9" width="700" class="mx-auto">
            <v-expand-transition>
              <div
                  v-if="hover"
                  class="d-flex transition-fast-in-fast-out grey darken-2 v-card--reveal text-h6 white--text"
                  style="height: 100%"
              >
                Я люблю делать разные вещи например спать кушать вкусно и играть доту 2 очень сожелею что попал в эту тусовку помогите вытащите оттуда я не хочу фармить лес 40 минут что бы проиграть о господе за что мне такие тиммейты
              </div>
            </v-expand-transition>
            </v-img>


            <v-expansion-panels>
            <v-expansion-panel>
              <v-expansion-panel-header color="#2E0F15">
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

              </v-card>
            </v-hover>
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
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}

h1{
  font: italic small-caps bold 60px/2 cursive;
  color:#BB9BB0;
  text-shadow: 2px 2px 0px #ffffff, 5px 4px 0px rgba(0,0,0,0.15), 2px 2px 2px rgba(206,89,55,0);
}
</style>
