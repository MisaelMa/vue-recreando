<script setup lang="ts">
import CardFlip from './components/CardFlip.vue';
const images = [
  {
    front: 'https://media.revistagq.com/photos/5f45010acb266484bb785c78/1:1/w_720,h_720,c_limit/dragon-ball-z.jpg',
    back: 'https://i.ebayimg.com/images/g/GnoAAOSwEiBhD6qo/s-l1200.jpg',
  },
  {
    front: 'https://w0.peakpx.com/wallpaper/772/329/HD-wallpaper-modo-sannin-konoha-modo-sabio-naruto-naruto-modo-sabio-naruto-shippuden-naruto-uzumaki-naruto-vs-pain-pain-thumbnail.jpg',
    back: 'https://vignette.wikia.nocookie.net/naruto/images/c/c7/Naruto_Modo_Sabio_de_lso_Seis_Caminos_Manga_HD.png/revision/latest/scale-to-width-down/300?cb=20160305031057&path-prefix=es',
  },
  {
    front: 'https://i.pinimg.com/474x/1b/ce/b4/1bceb4d04ceb5f5b7876bbf7f596d0f3.jpg',
    back: 'https://ih1.redbubble.net/image.4764345588.6663/flat,750x,075,f-pad,750x1000,f8f8f8.jpg',
  },
  {
    front: 'https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/4e14c4f4-5489-463c-89e0-7d4eadaedb9b/de8jd2u-bb134394-be90-4f66-9c91-5ddfdfd226cb.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzRlMTRjNGY0LTU0ODktNDYzYy04OWUwLTdkNGVhZGFlZGI5YlwvZGU4amQydS1iYjEzNDM5NC1iZTkwLTRmNjYtOWM5MS01ZGRmZGZkMjI2Y2IuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.q_t2Z0UqPdLB583GG25z_joYPJWwIc3FJqQBVAA0KDA',
    back: 'https://http2.mlstatic.com/D_NQ_NP_917241-MLM54437662885_032023-O.webp'
  }
]

</script>

<template>
  <div style="text-align: center;">
    <h1  style="font-size: 50px;">3D Card Flip Effect</h1>
  </div>
  <div class="grid">
    <template v-for="(image, i) of images" :key="i">
      <CardFlip>
        <template #front>
          <img :src="image.front" width="200" height="300"/>
        </template>
        
        <template #back>
          <img :src="image.back" width="200" height="300"/>
        </template>
      </CardFlip>
    </template>
  </div>

</template>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
}

.grid {
  padding: 100px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}
</style>
