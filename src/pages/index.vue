<script setup lang="ts">
import { ref } from 'vue'
const sectionOpen = ref(0)
</script>

<template>
  <h1 class="text-2xl">Bonjour monde !</h1>
  <section>
    <button 
    class="text-xl"
    @pointerdown="sectionOpen = sectionOpen===1?0:1"
    >bouton 1
    </button>
    <p
    v-show="sectionOpen===1">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Totam nisi odio vitae consectetur, neque voluptate nam earum fugiat blanditiis, animi unde deserunt soluta tenetur, recusandae molestiae quasi sapiente pariatur nostrum.</p>
  </section>
  <section>
    <button
    class="text-xl"
    @pointerdown="sectionOpen = sectionOpen===2?0:2"
    >bouton 2
    </button>
    <p
    v-show="sectionOpen===2">Dolore officia pariatur, accusamus vero quibusdam consequuntur necessitatibus voluptatibus nobis fugit a eos omnis repellendus. Magnam, porro voluptates. Saepe adipisci est corporis commodi eaque nulla eveniet illo esse recusandae animi!</p>
  </section>
  <section>
    <button
    class="text-xl"
    @pointerdown="sectionOpen = sectionOpen===3?0:3">bouton 3
    </button>
    <p
    v-show="sectionOpen===3">
    Sed, iusto aspernatur ipsa incidunt, minima fugit necessitatibus sapiente quo iure delectus doloremque officia voluptatibus ipsam inventore. Molestias eius molestiae quia praesentium placeat sequi ut repellendus velit, accusantium facere voluptate?</p>
  </section>
</template>
