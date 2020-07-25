<template>
    <div id="MainContent">
        <carousel :per-page="1" :paginationEnabled="false" height="100%">
            <slide>
                <HomePage></HomePage>
            </slide>
        </carousel>
    </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
import HomePage from './HomePage.vue';

export default {
  name : "MainContent",
  components: {
    Carousel,
    Slide,
    HomePage
  }
};
</script>

<style scoped>
#MainContent{
    width: 100%;
    height: calc(100% - 100px);
}
.VueCarousel{
    height: 100%;
}

</style>

<style>
.VueCarousel-wrapper{
    height: 100%;
}
.VueCarousel-inner{
    height: 100% !important;
}
</style>