<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      absolute
      color="deep-purple accent-4"
      dark
      scroll-target="#scrolling-techniques-6"
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Meus Projetos</v-toolbar-title>

      <v-spacer></v-spacer>

      <!-- <v-checkbox
        v-model="collapseOnScroll"
        color="white"
        hide-details
      ></v-checkbox> -->
      <v-checkbox
        v-model="ads"
        label="Ads"
        color="red"
        hide-details
        v-on:click="$emit('switch-ads', ads)"
      ></v-checkbox>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-6"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 8vh;"></v-container>
    </v-sheet>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      collapseOnScroll: true,
      ads:false
    }),
  }
</script>