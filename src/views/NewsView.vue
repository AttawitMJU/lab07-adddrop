<template>
  <v-btn class="ma-2" color="primary" @click="addNews()">
    Accept
    <v-icon end icon="mdi-checkbox-marked-circle"></v-icon>
  </v-btn>
  {{ news.newsList }}
  <v-container class="d-flex flex-wrap justify-start">
    <v-card
      class="ma-2"
      max-width="300"
      v-for="news in news.newsList"
      :key="news.id"
    >
      <v-img
        :src="'https://picsum.photos/200/300?random=' + news.id"
        height="200px"
        cover
      ></v-img>

      <v-card-title> {{ news.id }} {{ news.title }}</v-card-title>

      <v-card-subtitle> 1,000 miles of wonder </v-card-subtitle>

      <v-card-actions>
        <v-btn color="orange-lighten-2" variant="text"> Explore </v-btn>

        <v-spacer></v-spacer>

        <v-btn
          :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
          @click="show = !show"
        ></v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>

          <v-card-text>
            I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card></v-container
  >
</template>

<script setup>
import { ref } from "vue";
import { newsStore } from "@/stores/news";
const news = newsStore();
const show = ref(false);
function addNews() {
  news.newsList.push({ id: news.newsID, title: "Hello" });
}
</script>
