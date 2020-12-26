<template>
    <div id="CoverArtSection">
        <vuescroll>
            <div id="CoverArtArea">
                <cover v-for="cover in Covers" :key="cover.id" :url="cover.url" :description="cover.description">
                </cover>
            </div>
        </vuescroll>
    </div>
</template>

<script>
import Cover from '../Cover.vue'

import vuescroll from 'vuescroll/dist/vuescroll-native';

import boneCover from "./../../assets/BoneCover2.png"
import footBoneCover from "./../../assets/jbmr.2961.png"
import vortexCover from "./../../assets/jbmr.3764.png"


export default {
name : "CoverArt",
data : () => ({
    ops: {
          vuescroll: {detectResize: false},
          scrollPanel: {},
          rail: {},
          bar: {}
    },
    Covers : [
        {
            id : 0,
            url : boneCover,
            description : "<div>Ions such as calcium and phosphate are used in myriad key metabolic processes, and are central to life itself. However, their abundance and propensity to adversely precipitate as mineral requires a generalized inhibition. Selective removal of such inhibition (“inhibiting the inhibitor”) to allow mineralization can be used to define the size, shape and layout of an organism (from in utero through to adulthood). As part of this process there is the third tier of mineralization regulation – the fine interfacial enzyme-stenciling control that provides refinement for mechanical resilience, metabolic responsiveness, morphological precision and sensitivity to loading, to name a few, that apparently can distinguish life from death, and health from disease.</div>",
        },
        {
            id : 1,
            url : vortexCover,
            description : "<div>Vortex by Object Research Systems. This image shows the interior of a proximal femur of a sheep. The specimen was imaged usingmicro-computed tomography, and then surface-rendered using Dragonfly software. The spiraling orientation of the trabecular trusses, andthe transition of trabecular texture from a robust to a delicate fabric, create an impression of a dynamic vortex within the bone’s interior.</div>",
        },
        {
            id : 2,
            url : footBoneCover,
            description : "<div>Golden Lotus. Top panels: three-dimensional reconstruction by micro-computed tomography of a bound foot (museum specimen, the Royal College of Surgeons, London, UK) showing anatomical structure and relationships for both soft tissues (orange) and skeletal elements (yellow). Bottom left: close-up view of the left foot of a 75 year old woman who had her feet deformed at the age of 7 years. Courtesy of Jo Farrell (Jo Farrell Photography, <a href=http://www.livingherstoryphotography.com>http://www.livingherstoryphotography.com</a>). Bottom right: an embroidered “Golden Lotus” shoe occasionally worn by a woman having bound feet (courtesy of the Museums at the Royal College of Surgeons, London, UK).</div>",
        }
    ],
    }),
    components : {
        vuescroll,
        Cover
    }
}
</script>

<style scoped>

#CoverArtSection{
    height: 100%;
    width: 100%;
    padding: 50px;
}

#CoverArtArea{
    display: grid;
    width: 100%;
    height: 100%;
    grid-template: '.   .   .' 1fr /
                    1fr 1fr 1fr;
    column-gap: max(5%, 50px );
}

</style>