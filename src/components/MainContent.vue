<template>
    <div id="MainContent">
        <carousel :per-page="1" :paginationEnabled="false" @page-change="$emit('select',$event)" :value="activeID">
            <slide>
                <home-page @go-next="$emit('select',activeID+1)" ></home-page>
            </slide>
            <slide>
                <bio></bio>
            </slide>
            <slide>
                <publictions></publictions>
            </slide>
            <slide>
                <cover-art></cover-art>
            </slide>
        </carousel>
    </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
import HomePage from './sections/HomePage.vue';
import Bio from './sections/Bio.vue';
import CoverArt from './sections/CoverArt.vue';
import Publictions from './sections/Publictions.vue';


export default {
  name : "MainContent",
  props: {
      activeID : Number
  },
  components: {
    Carousel,
    Slide,
    HomePage,
    Bio,
    Publictions,
    CoverArt,
  }
};
</script>

<style scoped>
#MainContent{
    --padding : 0px;
    width: calc(100% - 2*var(--padding));
    height: calc(100% - 100px - 2*var(--padding));
    background-image: url("../assets/New background v2.png");
    background-size: contain;
    padding: var(--padding);
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