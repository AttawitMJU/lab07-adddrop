<script setup>
import {  RouterView } from "vue-router";
// import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <v-app>
    <v-app-bar
      color="teal-darken-4"
      image="https://picsum.photos/1920/1080?random"
    >
      <template v-slot:image>
        <v-img
          gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
        ></v-img>
      </template>

      <template v-slot:prepend>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </template>

      <v-app-bar-title>Title</v-app-bar-title>

      <v-spacer></v-spacer>
      <v-btn variant="text" to="/"> เมนู</v-btn>
      <v-btn variant="text" to="/news"> ข่าว </v-btn>
      <v-btn variant="text" to="/plan"> แผนการเรียน </v-btn>
      <v-btn variant="text" to="/adddrop"> เพิ่มถอนรายวิชา</v-btn>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <!-- <v-navigation-drawer>...</v-navigation-drawer> -->

    <v-main>
      <v-container><RouterView /></v-container
    ></v-main>
  </v-app>
</template>
