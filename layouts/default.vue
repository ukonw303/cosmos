<template>
  <v-app dark>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<style>
  .theme--dark.v-application {
    background-image:url('https://i0.wp.com/www.spaceweather.com/swpod2010/22sep10/globaleruption3.gif');
    background-size: cover;
}
  h1{
        font-family: 'Amatic SC', cursive;
        color: #000000;
}
  h2{
        font-family: 'Amatic SC', cursive;
        color:#212121;
}
  .mor{
        font-family: 'Sansita Swashed', cursive;
        color:#ffffff;
        font-size: 6rem;
        text-align: center;
}
</style>
