<script setup lang="ts">
import Item from './Item.vue'
import IconHoney from './icons/IconHoney.vue'
import Gallery from './Gallery.vue'
import IconHeart from './icons/IconHeart.vue'


</script>

<template>
  <Item>
    <template #icon>
      <IconHoney/>
    </template>
    <template #heading>Présentation</template>

    Le miel est extrait par mes soins à Hastière près de Dinant et Givet. Je m'efforce de produire un miel de qualité
    supérieure tout en respectant la nature et en ne traitant pas les abeilles avec des produits chimiques nocifs. Vous
    pouvez être sûr que le miel est sain et savoureux. N'hésitez pas à
    <RouterLink to="/about">me contacter</RouterLink>
    si vous avez des questions ou si vous souhaitez acheter du miel de printemps ou d'été. Son prix de vente est de 7
    euros par pot de 500g. Merci de soutenir les apiculteurs locaux !<br/><br/>
    <Gallery></Gallery>
  </Item>


  <Item>
    <template #icon>
      <IconHeart/>
    </template>
    <template #heading>Suivez moi sur Facebook !</template>

    Suivez <a href="https://www.facebook.com/Mielhermetonsurmeuse" rel="noopener">la page Facebook</a> de
    Hermeton-sur-Miel pour rester au courant de mes aventures apicoles et découvrir mes délicieux produits!🐝
  </Item>
</template>
