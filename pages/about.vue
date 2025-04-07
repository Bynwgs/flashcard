<template>
  <div class="flex flex-col min-h-screen bg-gray-100">
    <Navbar />
    <main class="flex-grow p-8">
      <h1 class="text-4xl font-bold mb-4">About</h1>
      <p class="text-gray-700 text-xl mt-5 pb-5">
        This is a simple flashcard app I created to help students studying A-Level Chemistry. To start, tap a card to flip it, revealing all the key-points and concepts you have learned.
      </p>
      <div class="flex justify-center mt-10 rounded-xl">
        <img class="scale-125" src="/images/chemistry.jpg" alt="Chemistry Textbook">
      </div>
      
    </main>
    <Footer />
  </div>
</template>

<script setup>

</script>

<style scoped>

</style>