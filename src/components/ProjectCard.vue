<template>
  <div class="card">
  <v-card max-width="375" outlined>
    <v-responsive class="pt-4">
      <v-img :src=icon height="100" width="100"></v-img>
    </v-responsive>

    
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title class="headline mb-1 title">{{name}}</v-list-item-title>
        <v-list-item-subtitle class="description">{{description}}</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar tile size="80" color="grey"></v-list-item-avatar>
    </v-list-item>

  </v-card>
  </div>
</template>

<script>
  export default {
    name: 'ProjectCard',
    props:['name', 'description', 'icon'],

    data: () => ({
    }),
  }
</script>

<style scoped>
.card{
  padding: 10px;
}

.title{
  font-weight: bold;
  font-size: 300%;
}
.description{
  font-size: 150%;
}
</style>