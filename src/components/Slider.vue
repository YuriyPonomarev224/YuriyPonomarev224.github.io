<template>
  <vueper-slides
  class="no-shadow"
  :visible-slides="3"
  slide-multiple
  :gap="3"
  :slide-ratio="1 / 4"
  :dragging-distance="200"
  :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }">
  <vueper-slide v-for="(slide, i) in slides" :key="i" :title="slide.title" :content="slide.content" :image="slide.image" :href="slide.content" />
</vueper-slides>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'
export default {
    name:"SliderMain",
    components: { VueperSlides, VueperSlide },
    data: () => ({
        slides: [
            {
            title: '1',
            content: 'ad',
            image: require('../assets/img/Item_1.png') ,
            link: "https://google.com"
            },
            {
            title: '2',
            content: 'href="https://google.com"',
            image: require('../assets/img/Item_2.png') 
            },
            {
            title: '3',
            content: 'ALOE',
            image: require('../assets/img/Item_3.png') 
            },
            {
            title: 'Slide #1',
            content: 'ALOE'
            },
            {
            title: 'Slide #1',
            content: 'ALOE'
            },
            {
            title: 'Slide #1',
            content: 'ALOE'
            }
        ]
    })
}
</script>

<style lang="scss">
.vueperslides {
    max-width: 90%;
    margin: 0 auto;
    height: 490px;
    &__bullets {
        display: none;
    }
}
.vueperslide {
    &__title {
        position: relative;
        top: 200px;
    }
}
</style>