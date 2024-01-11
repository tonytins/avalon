<template>
  <div class="page">
    <div class="sidebar bg-blue-900 text-left">
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

<style scoped>
.page {
  position: relative;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1;
}

.sidebar {
  width: 50px;
  height: 100vh;
  position: sticky;
  top: 0;
}

@media (min-width: 641px) {
  .page {
    flex-direction: row;
  }
}
</style>
