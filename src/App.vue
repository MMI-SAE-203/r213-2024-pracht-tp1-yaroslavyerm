<script setup lang="ts">
import { onErrorCaptured } from 'vue'
import { RouterLink, RouterView } from 'vue-router/auto'
onErrorCaptured((err, instance, info) => {
  console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
  return true
})
import { ref } from 'vue'
const menuIsOpen = ref(false)
</script>

<template>
  <div class="bg-gray-800 h-screen">
    <header>
      <button
        aria-controls="mainNav"
        aria-expanded="true"
        class="rounded-full border-2 border-red-600 bg-red-300 px-2"
        @pointerdown="menuIsOpen = !menuIsOpen"
        >
        menu
      </button>
      <Transition
        class="transition-transform duration-500"
        enter-from-class="-translate-x-full"
        enter-to-class="translate-x-0"
        leave-active-class="-translate-x-full"
        >
      <nav v-show="menuIsOpen" id="mainNav">
        <ul>
          <li><RouterLink to="/">Accordeon</RouterLink></li>
          <li><RouterLink to="/donnees">Données</RouterLink></li>
        </ul>
      </nav>
      </Transition>
    </header>
    <RouterView v-slot="{ Component }">
      <Suspense>
        <component :is="Component" />
      </Suspense>
    </RouterView>
  </div>
</template>
