<template>
    <div id="CoverArtSection">
        <vue-custom-scrollbar class="scroll-area"  :swipeEasing="true">
            <div id="CoverArtArea">
                <div class="Cover" v-for="cover in covers" :key="cover.id">
                    <img :src="cover.url" :class="{ first: cover.id==0, second: cover.id==1, third: cover.id==2}">
                    <div class="TextArea">
                        {{ 
                        cover.description  
                        }}
                    </div>
                </div>
            </div>
        </vue-custom-scrollbar>
    </div>
</template>

<script>

import vueCustomScrollbar from 'vue-custom-scrollbar'

import boneCover from "./../../assets/BoneCover2.png"
import footBoneCover from "./../../assets/jbmr.2961.png"
import vortexCover from "./../../assets/jbmr.3764.png"


export default {
name : "CoverArt",
data : () => ({
    covers : [
        {
            id : 0,
            url : boneCover,
            description : "Ions such as calcium and phosphate are used in myriad key metabolic processes, and are central to life itself. However, their abundance and propensity to adversely precipitate as mineral requires a generalized inhibition. Selective removal of such inhibition (“inhibiting the inhibitor”) to allow mineralization can be used to define the size, shape and layout of an organism (from in utero through to adulthood). As part of this process there is the third tier of mineralization regulation – the fine interfacial enzyme-stenciling control that provides refinement for mechanical resilience, metabolic responsiveness, morphological precision and sensitivity to loading, to name a few, that apparently can distinguish life from death, and health from disease.",
        },
        {
            id : 1,
            url : vortexCover,
            description : "Vortex by Object Research Systems. This image shows the interior of a proximal femur of a sheep. The specimen was imaged usingmicro-computed tomography, and then surface-rendered using Dragonfly software. The spiraling orientation of the trabecular trusses, andthe transition of trabecular texture from a robust to a delicate fabric, create an impression of a dynamic vortex within the bone’s interior.",
        },
        {
            id : 2,
            url : footBoneCover,
            description : "Golden Lotus. Top panels: three-dimensional reconstruction by micro-computed tomography of a bound foot (museum specimen, the Royal College of Surgeons, London, UK) showing anatomical structure and relationships for both soft tissues (orange) and skeletal elements (yellow). Bottom left: close-up view of the left foot of a 75 year old woman who had her feet deformed at the age of 7 years. Courtesy of Jo Farrell (Jo Farrell Photography, <a href=\"http://www.livinghistory.photography/\"> http://www.livinghistory.photography/ </a>). Bottom right: an embroidered “Golden Lotus” shoe occasionally worn by a woman having bound feet (courtesy of the Museums at the Royal College of Surgeons, London, UK).",
        }
    ]
}),
computed : {

},
components : {
    vueCustomScrollbar
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
    height: 120%;
    grid-template-columns: 30% 30% 30%;
    column-gap: 5%;
    row-gap: 10%;
    grid-template-rows: 100%;
}

.Cover{
    display: grid;
    grid-template-columns: 100%;
    grid-template-rows: auto 1fr 20px;
    height: 100%;
}


.Cover img{
    display: inline-block;
    width: 100%
}

.TextArea{
    background-color: var(--main-color);
    border-radius: 0px 0px 5px 5px;
    font-size: 12px;
}

</style>