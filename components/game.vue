<template>
  <div class="flex flex-col items-center justify-center py-10 gap-6">
    <h2 class="text-2xl font-semibold">Flashcards</h2>
    
    <Flashcard  v-if="currentCard" :flashcard="currentCard" :flipped="flipped" @toggle-flip="flipped = !flipped" />

    <div class="flex gap-4 mt-4">
      <button
        @click="prevCard"
        class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 transition"
        :disabled="currentIndex === 0"
      >
        Previous
      </button>
      <button
        @click="nextCard"
        class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600 transition"
        :disabled="currentIndex === flashcards.length - 1"
      >
        Next
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const flashcards = [
  { question: 'What is atomic mass unit?', answer: 'One-twelfth the mass of a carbon-12 atom' },
  { question: 'What is empirical formula?', answer: 'Simplest whole number ratio of the elements present in one molecule or formula unit of the compound' },
  { question: 'What is molecular formula?', answer: 'Actual number of atoms of each element present in one molecule of a compound' },
  { question: 'What is covalent bond?', answer: 'Electrostatic attraction between nuclei of two atoms and shared pair of electrons' },
  { question: 'What is electronegativity?', answer: 'Ability of an atom that is covalently bonded to another atom to attract the bond pair of electrons towards itself' },
  { question: 'What is disproportionation?', answer: 'Reaction where a species is oxidised and reduced simultaneously' },
  { question: 'What is dynamic equilibrium?', answer: 'Rate of forward and reverse reaction being equal and the concentration of reactants and products remain constant over time' },
  { question: 'What is a nucleophile?', answer: 'A species with a lone pair of electrons, which will attack the electron deficient centre of a molecule' },
  { question: 'What is stereoisomerism?', answer: 'Molecules with the same molecular formula and strutural formula with different arrangement of atoms in space' },
  { question: 'What is addition reaction?', answer: 'A reaction where two or more compounds react to form a single product' },
]

const currentIndex = ref(0)
const flipped = ref(false)

const currentCard = computed(() => flashcards[currentIndex.value])

const nextCard = () => {
  if (currentIndex.value < flashcards.length - 1) {
    currentIndex.value++
    flipped.value = false 
  }
}

const prevCard = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--
    flipped.value = false 
  }
}
</script>
