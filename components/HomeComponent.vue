<template>
  <vs-row>
    <vs-col
      v-for="(col, index) in 4"
      :key="index"
      vs-type="flex"
      vs-justify="center"
      vs-align="center"
      w="3"
    >
      <CardsItem />
      <CardsItem />
      <CardsItem />
    </vs-col>
  </vs-row>
</template>
