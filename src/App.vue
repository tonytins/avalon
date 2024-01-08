<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import NavMenu from "./components/NavMenu.vue";
</script>

<template>
  <div class="page">
    <div class="sidebar">
      <NavMenu />
    </div>

    <main>
      <div class="top-row px-4">

      </div>

      <article class="content px-4">
        <div class="container">
          <h1>Hello, world!</h1>

          Welcome to your new app.
        </div>
      </article>
    </main>
  </div>
</template>

<style scoped>
.logo.vite:hover {
  filter: drop-shadow(0 0 2em #747bff);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #249b73);
}
</style>
