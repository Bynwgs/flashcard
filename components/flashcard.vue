<template>
  <div
    class="w-96 h-64 bg-white shadow-xl rounded-2xl flex items-center justify-center text-center px-4 py-2 cursor-pointer"
    @click="$emit('toggle-flip')"
  >
    <div class="text-lg">
      {{ flipped ? flashcard.answer : flashcard.question }}
    </div>
  </div>
</template>

<script setup>
defineProps({
  flashcard: Object,
  flipped: Boolean
})

defineEmits(['toggle-flip'])
</script>

