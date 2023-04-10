<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="honey">{{ msg }}</h1>
    <h3>
      Bienvenue sur le site de Laurent Dispa, apiculteur à Hastière, près de Dinant, en Belgique. <br/> <br/>
      Découvrez ma passion pour les abeilles et les produits issus de mes propres ruches, situées dans la vallée de l'Hermeton.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
