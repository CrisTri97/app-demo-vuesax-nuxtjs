<template>
  <vs-row>
    <vs-col
      v-for="user in users"
      :key="user.id"
      vs-type="flex"
      vs-justify="center"
      vs-align="center"
      w="3"
    >
      <CardsItem :user="user" />
    </vs-col>
  </vs-row>
</template>

<script>
import { users } from '~/mockData/user'
export default {
  data: () => ({
    users,
  }),
}
</script>
