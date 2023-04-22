<script>
import VueEasyLightbox from 'vue-easy-lightbox'
import {defineComponent, ref} from 'vue'
import jars from '@/assets/images/jars.jpg'
import girl from '@/assets/images/girl.jpg'
import hives from '@/assets/images/hives.jpg'
import beekeeper from '@/assets/images/beekeeper.jpg'
import sheep from '@/assets/images/sheep.jpg'
import bees from '@/assets/images/bees.jpg'


export default defineComponent({
  components: {
    VueEasyLightbox
  },
  setup() {
    const visibleRef = ref(false)
    const indexRef = ref(0) // default 0
    const imgsRef = ref([
      jars,
      girl,
      hives,
      beekeeper,
      sheep,
      bees])

    const onShow = () => {
      visibleRef.value = true
    }
    const showMultiple = (index) => {
      indexRef.value = index // index of imgList
      onShow()
    }
    const onHide = () => (visibleRef.value = false)

    return {
      visibleRef,
      indexRef,
      imgsRef,
      showMultiple,
      onHide
    }
  }
})
</script>
<template>
  <div>
    <button @click="showMultiple(0)"><img src="@/assets/images/thumbnails/jars.jpg" alt="Pots de miel"/></button>
    <button @click="showMultiple(1)"><img src="@/assets/images/thumbnails/girl.jpg" alt="Fille en tenue d'apiculteur"/></button>
    <button @click="showMultiple(2)"><img src="@/assets/images/thumbnails/hives.jpg" alt="Ruches"/></button>
    <button @click="showMultiple(3)"><img src="@/assets/images/thumbnails/beekeeper.jpg" alt="Apiculteur"/></button>
    <button @click="showMultiple(4)"><img src="@/assets/images/thumbnails/sheep.jpg" alt="Moutons devant des ruches"/></button>
    <button @click="showMultiple(5)"><img src="@/assets/images/thumbnails/bees.jpg" alt="Abeilles"/></button>
    <vue-easy-lightbox
        :visible="visibleRef"
        :imgs="imgsRef"
        :index="indexRef"
        @hide="onHide"
    ></vue-easy-lightbox>
  </div>
</template>


<style scoped>
button {
  padding: 0;
  border: none;
  background: none;
}

img {
  border-radius: 15%;
  object-fit: cover;
  background-position: center center;
  background-repeat: no-repeat;
  overflow: hidden;
  height: 120px;
  width: 120px;
  margin: auto;
  padding: 5px;
  cursor: pointer;
}

@media (min-width: 1024px) {
  img {
    height: 140px;
    width: 140px;
  }
}



</style>