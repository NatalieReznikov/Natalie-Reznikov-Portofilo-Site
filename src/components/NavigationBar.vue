<template>
    <div id="NavBar">
        <SectionButton v-for="slide in Slides" :key="slide.id">
            
        </SectionButton>
    </div>
</template>

<script>
import SectionButton from "./SectionButton.vue";

export default {
    name : "NavBar",
    props : {
        Slides: {
            id : Number,
            msg : String,
            press : Function
        }
    },
    components : {
        SectionButton
    }
}
</script>

<style scoped>
#NavBar{
    background-color: #282C34;
    width: 100%;
    height: 100px;
    padding: 5px;
}
</style>