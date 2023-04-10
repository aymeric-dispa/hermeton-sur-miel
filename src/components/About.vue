<script setup lang="ts">
import Item from './Item.vue'
import Price from './icons/Price.vue'
import IconHeart from './icons/IconHeart.vue'
</script>

<template>
  <Item>
    <template #icon>
      <Price/>
    </template>
    <template #heading>Tarifs</template>
    Le miel est vendu en pot de 500g au prix de 7 euros. Ce prix reflète la qualité supérieure du miel et permet de
    couvrir le processus d'extraction manuelle qui garantit un produit naturel et de grande qualité. Je suis convaincu
    que vous apprécierez ce miel artisanal, et je suis fier de pouvoir vous l'offrir à un prix abordable.
  </Item>
  <Item>
    <template #icon>
      <IconHeart/>
    </template>
    <template #heading>Contact</template>
    Vous pouvez me contacter via e-mail a l'adresse <a
      href="mailto: laurent.dispa@gmail.com">laurent.dispa@gmail.com</a> afin de collecter votre miel à Hastière, près
    de Dinant. Alternativement, vous pouvez aussi me contacter directement via <a
      href="https://www.facebook.com/Mielhermetonsurmeuse" rel="noopener">la page Facebook</a> de Hermeton-sur-Miel.
    Profitez-en pour me suivre afin de rester au courant de mes aventures apicoles et découvrir mes délicieux produits!🐝
    <br/><br/>
    <iframe
        title="Hermeton sur miel map"
        width="100%"
        height="200"
        style="border:0"
        loading="lazy"
        allowfullscreen
        referrerpolicy="no-referrer-when-downgrade"
        src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBbecHokUHv9V6ZfLHp44tzoayhfa0sS0Q&q=Vieille+Route+de+Givet+Hastiere+Belgium">
    </iframe>
  </Item>

</template>