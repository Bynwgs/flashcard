<template>
  <div class="min-h-screen bg-gray-100 flex flex-col">
    <Navbar />
    <main class="flex flex-grow flex-col items-center justify-center p-8 text-center">
      <h1 class="text-4xl font-bold mb-6">Welcome to Chemistry 101</h1>
      <p class="text-xl text-gray-700 mb-6">Start now to unlock Chemistry!</p>
      <NuxtLink to="/flashcards" class="bg-blue-500 hover:bg-blue-600 text-white px-6 py-3 rounded-xl transition text-lg">Start Flashcards</NuxtLink>
    </main>
    <Footer />
  </div>
  

  
</template>

<script setup>



</script>

<style scoped>

</style>