<script setup lang="ts">
import BaseCard from './composantsCommuns/BaseCard.vue'
import imgEchauffement from './assets/images/echauffement.png'
import imgTonPrestance from './assets/images/ton-prestance.png'
import imgPhraseCourte from './assets/images/phrase-courte.png'
import imgPivot from './assets/images/pivot.png'
import imgTraducteur from './assets/images/traducteur.png'
import imgJouteVerbale from './assets/images/joute.png'

const descriptionEchauffement = 'Echauffe toi en répettant des phrases le plus rapidement possible.'
const titleEchauffement = 'Echauffement'

const descriptionTonPrestance = 'Raconter une anecdote banale en ajutant ton ton'
const titleTonPrestance = 'Ton & Prestance'

const descriptionPhraseCourte = 'Apprends à définir les mots en une phrase courte'
const titlePhraseCourte = 'Phrase Courte'

const descriptionPivot = 'Essaie de relier deux mots opposés'
const titlePivot = 'Le Pivot'

const descriptionTraducteur = 'Transforme une phrase en 3 niveaux de langage différents'
const titleTraducteur = 'Le Traducteur'

const descriptionJouteVerbale = 'Affronte un adversaire sur un thème donné'
const titleJouteVerbale = 'Joute Verbale'

</script>

<template>
  <div class="ligne-cards">
    <BaseCard
      :title="titleEchauffement"
      :imgSrc="imgEchauffement"
      :description="descriptionEchauffement"
    />
    <BaseCard
      :title="titleTonPrestance"
      :imgSrc="imgTonPrestance"
      :description="descriptionTonPrestance"
    />
    <BaseCard
      :title="titlePhraseCourte"
      :imgSrc="imgPhraseCourte"
      :description="descriptionPhraseCourte"
    />
    <BaseCard
      :title="titlePivot"
      :imgSrc="imgPivot"
      :description="descriptionPivot"
    />
    <BaseCard
      :title="titleTraducteur"
      :imgSrc="imgTraducteur"
      :description="descriptionTraducteur"
    />
    <BaseCard
      :title="titleJouteVerbale"
      :imgSrc="imgJouteVerbale"
      :description="descriptionJouteVerbale"
    />
  </div>
</template>

<style scoped>
.ligne-cards {
  display: flex;
  flex-wrap: wrap;
}

</style>
