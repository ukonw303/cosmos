<template>
  <div class="mt-12">
    <v-card align="center" color="#FF8A65">
      <v-row>
        <v-col md="5">
          <v-img :src="this.$route.params.id.url" max-width="100%" />
          {{ this.$route.params.id.url }}
        </v-col>
        <v-col md="7">
          <h1>{{ this.$route.params.id.title }}</h1><br>
          <div align="left">
            <h2>Date : {{ this.$route.params.id.date }} </h2><br>
            <h2>Explanation : {{ this.$route.params.id.explanation }}</h2>
          </div>
        </v-col>
      </v-row>
    </v-card>
  </div>
</template>
