<script setup lang="ts">
import { phrases } from '../data/phrasesEchauffement'
import { ref } from 'vue'

const jeuLance = ref(false)
const phraseActuelle = ref('')

const randomPhrase = () => {
  const index = Math.floor(Math.random() * phrases.length)
  phraseActuelle.value = phrases[index] || ''
}

const startGame = () => {
  jeuLance.value = true
  randomPhrase()
}

</script>

<template>
  <div class="echauffement-page">

    <!-- ECRAN 1 : Les consignes (S'affiche si jeuLance est faux) -->
    <div v-if="!jeuLance" class="ecran-consignes">
      <h1>Échauffement</h1>
      <p>
        Place un stylo (propre !) entre tes dents, à l'horizontale. <br>
        Le but est de prononcer les phrases qui vont s'afficher de la manière la plus distincte possible.
      </p>
      <button @click="startGame">Lancer l'échauffement</button>
    </div>

    <!-- ECRAN 2 : Le jeu (S'affiche si jeuLance est vrai) -->
    <div v-else class="ecran-jeu">
      <p class="phrase-texte">{{ phraseActuelle }}</p>
      <button @click="randomPhrase">Phrase Suivante</button>
    </div>

  </div>
</template>

<style scoped>
.echauffement-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
}

.phrase-texte {
  font-size: 24px;
  font-weight: bold;
  margin: 40px 0;
  color: #2c3e50;
  max-width: 600px;
}

button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 15px 30px;
  font-size: 18px;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #33996b;
}
</style>
