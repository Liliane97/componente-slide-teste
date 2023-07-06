<template>
  <div class="mb-2 my-sm-5 my-mdAndUp-5 px-3">
    <v-carousel
      cycle
      color="secondary"
      hide-delimiter-background
      height="200"
    >
      <template v-slot:prev="{ props }">
        <v-btn
          variant="text"
          icon="mdi mdi-chevron-left"
          color="secondary"
          @click="props.onClick"
        ></v-btn>
      </template>
      <template v-slot:next="{ props }">
        <v-btn
          variant="text"
          color="secondary"
          icon="mdi mdi-chevron-right"

          @click="props.onClick"
        ></v-btn>
      </template>
      <v-carousel-item v-for="s in 5" :key="s" eager>
        <v-card
        height="200"
          :ripple="false"
          color="blue"
          
        >
          {{ s }}
        </v-card>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>
