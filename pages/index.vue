<template lang="html">
  <div>
    <div class="mor">
      cosmos
    </div>
    <div>
      <v-text-field v-model="DayID" type="text" label="Day" color="#FF8A80" />
      <v-text-field v-model="MonthID" type="text" label="Month" color="#FF8A80" />
      <v-text-field v-model="YearID" type="text" label="Year" color="#FF8A80" />
      <v-btn color="#E53935" @click="nanaha">
        Search
        <v-icon>mdi-android</v-icon>
      </v-btn>
      </v-date-picker>
    </div>
    <v-divider class="mt-2 mb-2" />
    <div v-for="list in ID" :key="list.date">
      <!-- {{list}} -->
      <nuxt-link :to=" {name: 'product-id', params: { id: list }} ">
        <img
          style="max-width:100%"
          :src="list.hdurl"
        >
      </nuxt-link>
    </div>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  data () {
    return {
      ID: null,
      DayID: '',
      MonthID: '',
      YearID: '',
      DateID: ''
    }
  },
  methods: {
    nanaha () {
      const url = 'https://api.nasa.gov/planetary/apod?date=' + this.YearID + '-' + this.MonthID + '-' + this.DayID + '&hd=true&api_key=iK6QWVlZ9w0RUsSNWob3UL5KcXFehRlXBHvKuW6p'
      axios.get(url).then((response) => {
        this.ID = response
      })
    }
  }
}
</script>
<style lang="css" scoped></style>
