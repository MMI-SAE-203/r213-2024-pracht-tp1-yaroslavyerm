<script setup lang="ts">
import { ref } from 'vue'
const sectionOpen = ref(0)
</script>

<template>
  <h1 class="text-4xl font-greycliff text-gray-100 font-bold ">Accordeon</h1>
  <div class="grid grid-cols-3 p-4 gap-4">
    <section class="">
      <button
      class="w-full text-xl font-greycliff text-gray-800 font-bold bg-gray-100 rounded-sm p-2 active:bg-gray-800 active:text-gray-100 active:border active:border-gray-100 hover:bg-gray-300 hover:text-gray-800 hover:border hover:border-gray-800"
      @pointerdown="sectionOpen = sectionOpen===1?0:1"
      >Bouton 1
      </button>
      <p
      v-show="sectionOpen===1"
      class="text-base text-balance font-medium text-gray-100"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Totam nisi odio vitae consectetur, neque voluptate nam earum fugiat blanditiis, animi unde deserunt soluta tenetur, recusandae molestiae quasi sapiente pariatur nostrum.</p>
    </section>
    <section class="">
      <button
      class="w-full text-xl font-greycliff text-gray-800 font-bold bg-gray-100 rounded-sm p-2 active:bg-gray-800 active:text-gray-100 active:border active:border-gray-100 hover:bg-gray-300 hover:text-gray-800 hover:border hover:border-gray-800"
      @pointerdown="sectionOpen = sectionOpen===2?0:2"
      >Bouton 2
      </button>
      <p
      class="text-base text-balance font-medium text-gray-100"
      v-show="sectionOpen===2">Dolore officia pariatur, accusamus vero quibusdam consequuntur necessitatibus voluptatibus nobis fugit a eos omnis repellendus. Magnam, porro voluptates. Saepe adipisci est corporis commodi eaque nulla eveniet illo esse recusandae animi!</p>
    </section>
    <section class="">
      <button
      class="w-full text-xl font-greycliff text-gray-800 font-bold bg-gray-100 rounded-sm p-2 active:bg-gray-800 active:text-gray-100 active:border active:border-gray-100 hover:bg-gray-300 hover:text-gray-800 hover:border hover:border-gray-800"
      @pointerdown="sectionOpen = sectionOpen===3?0:3">Bouton 3
      </button>
      <p
      class="text-base text-balance font-medium text-gray-100"
      v-show="sectionOpen===3">
      Sed, iusto aspernatur ipsa incidunt, minima fugit necessitatibus sapiente quo iure delectus doloremque officia voluptatibus ipsam inventore. Molestias eius molestiae quia praesentium placeat sequi ut repellendus velit, accusantium facere voluptate?</p>
    </section>
  </div>
</template>
