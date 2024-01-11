<template>
  <div class="page">
    <div class="sidebar">
      <SideBar />
    </div>

    <main>
      <article class="content px-4">
        <div class="container">
          <component :is="currentView" />
        </div>
      </article>
    </main>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import Home from './Home.vue'
import About from './About.vue'
import NotFound from './NotFound.vue'
import SideBar from './SideBar.vue'

const routes = {
  '/': Home,
  '/about': About
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})
</script>

<style scoped></style>
