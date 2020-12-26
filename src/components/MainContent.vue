<template>
    <div id="MainContent">
        <div ref="slider" class="keen-slider">
            <div class="keen-slider__slide number-slide1">
                <home-page @go-next="$emit('select', activeID+1)" ></home-page>
            </div>
            <div class="keen-slider__slide number-slide2">
                <bio></bio>
            </div>
            <div class="keen-slider__slide number-slide3">
                <publictions></publictions>
            </div>
            <div class="keen-slider__slide number-slide4">
                <cover-art></cover-art>
            </div>
        </div>
    </div>
</template>

<script>
import "keen-slider/keen-slider.min.css";
import KeenSlider from "keen-slider";


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
    HomePage,
    Bio,
    Publictions,
    CoverArt,
  },
  watch : {
    activeID : function(newVal) {
        this.slider.moveToSlideRelative(newVal, true);
    }

  },
  data : () => {
    return{
        slider: null
    }
  },
  mounted() {
    this.slider = new KeenSlider(this.$refs.slider, {
        initial: this.activeID,
        afterChange : slider => {
            this.$emit('select', slider.details().relativeSlide);
        }
    });
    this.slider.controls(false);
  },
  beforeDestroy() {
    if (this.slider) this.slider.destroy();
  }
};
</script>

<style scoped>
#MainContent{
    --padding : 0px;
    width: calc(100% - 2*var(--padding));
    height: calc(100% - 100px - 2*var(--padding));
    background-color: #1F1F1F;
    background-image: url("../assets/New background v3.png");
    background-size: 10%;
    padding: var(--padding);
}
.VueCarousel{
    height: 100%;
}

</style>

<style>
.keen-slider{
    height: 100%;
    user-select: unset;
}
.keen-slider__slide{
    height: 100% !important;
}
</style>