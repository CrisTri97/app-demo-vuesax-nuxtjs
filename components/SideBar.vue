<template>
  <div class="hidden">
    <vs-sidebar v-model="active" absolute open>
      <template #logo>
        <!-- ...img logo -->
      </template>
      <vs-sidebar-item id="home">
        <template #icon>
          <i class="bx bx-home"></i>
        </template>
        <NuxtLink to="/">
          Home
        </NuxtLink>
      </vs-sidebar-item>
      <vs-sidebar-item id="shopping">
        <template #icon>
          <i class="bx bxs-shopping-bags"></i>
        </template>
        <NuxtLink to="/addproduct">
          Add product
        </NuxtLink>
      </vs-sidebar-item>
      <vs-sidebar-item id="theme">
        <vs-switch v-model="active5" dark>
          <template #circle>
            <i v-if="!active5" class="bx bxs-moon"></i>
            <i v-else class="bx bxs-sun"></i>
          </template>
        </vs-switch>
      </vs-sidebar-item>
    </vs-sidebar>
  </div>
</template>

<script>
/* ✓ GOOD */
export default {
  name: 'SideBar',
  // ...
  data: () => ({
    active: 'home',
  }),
}
</script>
