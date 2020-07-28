<template>
    <div id="NavBar">
        <section-button v-for="slide in Slides" :key="slide.id" :id="slide.id" :msg="slide.msg" :activeID="activeID" @selected="$emit('select', slide.id)">
            
        </section-button>
    </div>
</template>

<script>
import SectionButton from "./SectionButton.vue";

export default {
    name : "NavBar",
    props : {
        Slides: Array,
        activeID : Number
    },
    
    components : {
        SectionButton
    }
    
}
</script>

<style scoped>
#NavBar{
    background-color: #282C34;
    width: calc(100% - 10px);
    height: 90px;
    padding: 5px;
    display: flex;
}
</style>