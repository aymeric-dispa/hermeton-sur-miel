<script>
import VueEasyLightbox from 'vue-easy-lightbox'
import {defineComponent, ref} from 'vue'

export default defineComponent({
  components: {
    VueEasyLightbox
  },
  setup() {
    const visibleRef = ref(false)
    const hola = "helo"
    const indexRef = ref(0) // default 0
    const imgsRef = ref([
      "https://scontent-man2-1.xx.fbcdn.net/v/t39.30808-6/238734153_2917627928503464_5437107055800301520_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=730e14&_nc_eui2=AeEvLKmlXwtCnvEwL5FDSgru7ARPIE5nb9bsBE8gTmdv1o1_UpgkxHbLRuWI4JPPI_A&_nc_ohc=_mvV9OzZY0kAX-FySfF&_nc_ht=scontent-man2-1.xx&oh=00_AfBLtDunFfhwXiNHxjMiPryHc6Q_qBrCp5GbisdR8JzShQ&oe=6439A1AB",
      "https://scontent-man2-1.xx.fbcdn.net/v/t1.18169-9/27540408_1973029376296662_5878494138883573046_n.jpg?_nc_cat=103&ccb=1-7&_nc_sid=174925&_nc_eui2=AeEfbzr3MHsmXz6bQA9sMlCg6wHGPuBMTrjrAcY-4ExOuMgaOvbUKKxq4pxoEoFFLHQ&_nc_ohc=vW__2Hhs2IoAX_1sOY7&_nc_ht=scontent-man2-1.xx&oh=00_AfBIeIOz8NRU3mTUaikFNTFTZJld9IXn3XuQmL3C8ov3Ww&oe=645B3815",
      "https://scontent-man2-1.xx.fbcdn.net/v/t1.6435-9/101550833_2567031480229779_8701155755132190720_n.jpg?_nc_cat=100&ccb=1-7&_nc_sid=730e14&_nc_eui2=AeFXej8LX6W8Smgo9TEcvBE7WOV1uF-p3ttY5XW4X6ne2_WVjT72nEF1Ul6K8bz_RVc&_nc_ohc=Sf5GSs6FbAMAX_hcfEE&_nc_oc=AQmoYDMvYHJTwHpFWAqBmGJlrF7wE8NiKhkEr0qgMBYySqqFFNzyFGlS8bHzOt8BoMw&_nc_ht=scontent-man2-1.xx&oh=00_AfBaZosDGcSjCOB_1fsHmZwHjtpvEC9TiTJs-1AErjMxMA&oe=645A85E4",
      "https://scontent-man2-1.xx.fbcdn.net/v/t31.18172-8/11913881_1610683949197875_7625715548710395368_o.jpg?_nc_cat=104&ccb=1-7&_nc_sid=cdbe9c&_nc_eui2=AeGMxbCGOyKtDUxh1wMv0qY4lDj3ym4aspCUOPfKbhqykBR5Rg7gse_f23aNdMR1X24&_nc_ohc=xqIMJd7ZWz4AX_ixRyO&_nc_ht=scontent-man2-1.xx&oh=00_AfB4hlfm-ueTcldPHkLuPMJUs-WaQVD3IxdzIHh5i8m_TQ&oe=645A84EB",
      "https://scontent-man2-1.xx.fbcdn.net/v/t31.18172-8/10547941_1493702244229380_1895725556419672585_o.jpg?_nc_cat=110&ccb=1-7&_nc_sid=19026a&_nc_eui2=AeEQioLfqyuL0Lt-NZko_nFpXLp9v2np1Txcun2_aenVPLtkDmXcOAyc9wxUzDQ6KoI&_nc_ohc=pyJ88fpkbrkAX8DJrEy&_nc_ht=scontent-man2-1.xx&oh=00_AfBPp2o-4rtLOjwv8V0SOr88sQJtcWRlj60Kb2cXvqufWA&oe=645A6674",
      "https://scontent-man2-1.xx.fbcdn.net/v/t31.18172-8/14124258_1738044576461811_1492964982119172349_o.jpg?_nc_cat=106&ccb=1-7&_nc_sid=cdbe9c&_nc_eui2=AeFkCAmzOxLd7fxlHS3RvyEYg3Ie22eKhLqDch7bZ4qEuua2cAXqJ7d2wZ8girbLscw&_nc_ohc=toCNNmYfaoUAX-SuC5b&_nc_ht=scontent-man2-1.xx&oh=00_AfACA-1KopE5WVCIlbUF6g_ZRmytnD5WEuaMqCxIYw9k2g&oe=645A717D"
    ])

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
      onHide,
      hola
    }
  }
})
</script>
<template>
  <div>
    <button @click="showMultiple(0)"><img v-bind:src="imgsRef[0]" alt="Pots de miel"/></button>
    <button @click="showMultiple(1)"><img v-bind:src="imgsRef[1]" alt="Fille en tenue d'apiculteur"/></button>
    <button @click="showMultiple(2)"><img v-bind:src="imgsRef[2]" alt="Ruches"/></button>
    <button @click="showMultiple(3)"><img v-bind:src="imgsRef[3]" alt="Apiculteur"/></button>
    <button @click="showMultiple(4)"><img v-bind:src="imgsRef[4]" alt="Moutons devant des ruches"/></button>
    <button @click="showMultiple(5)"><img v-bind:src="imgsRef[5]" alt="Abeilles"/></button>
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