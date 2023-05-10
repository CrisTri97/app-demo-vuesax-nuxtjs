<template>
  <vs-card type="2">
    <template #title>
      <h3>{{ user.name }}</h3>
    </template>
    <template #img>
      <img src="https://vuesax.com/foto6.png" alt="" />
    </template>
    <template #text>
      <p>{{ user.email }}</p>
    </template>
    <template #interactions>
      <vs-button danger icon>
        <i class="bx bx-heart"></i>
      </vs-button>
      <vs-button class="btn-chat" shadow primary>
        <i class="bx bx-chat"></i>
        <span class="span"> 54 </span>
      </vs-button>
    </template>
  </vs-card>
</template>

<script>
export default {}
</script>

<script lang="ts">
interface User {
  id: number
  name: string
  username: string
  email: string
  website: string
}
import { PropType } from 'vue'
/* ✓ GOOD */
export default {
  name: 'CardsItem',
  props: {
    user: {
      type: Object as PropType<User>,
      required: true,
    },
  },
}
</script>
