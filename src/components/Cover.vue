<template>
  <div class="Cover">
    <img :src="url">
    <div class="TextArea">
      <svg width="28" height="10" xmlns="http://www.w3.org/2000/svg">
        <g>
          <title>background</title>
          <rect fill="none" id="canvas_background" height="602" width="802" y="-1" x="-1"/>
        </g>
        <g>
          <title>Layer 1</title>
          <path stroke="#6FEB95" id="svg_1" transform="rotate(-90 14.02941417694092,4.970588207244872) " stroke-linejoin="round" stroke-linecap="round" fill="none" d="m9.67647,18.26471l8.70588,-13.29412l-8.70588,-13.29412"/>
        </g>
      </svg>    
      <div v-html="description">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name : "Cover",
  props: {
    url : String,
    description : String
  }
}
</script>

<style scoped>
.Cover{
  position: relative;
  display: block;
  height: 100%;
  width: 100%;
  overflow: hidden;
}


.Cover img{
  display: inline-block;
  width: 100%;
  height: 100%;
}

.TextArea svg{
  top: 0px;
  margin: 1px auto 1px auto;
  display: block;
  position: relative;
}

.TextArea{
  padding: 5px;
  background-image: linear-gradient( rgba(40, 44, 52, 0.7), rgb(40, 44, 52, 1) 33%);
  border-radius: 5px 5px 0px 0px;
  font-size: min(0.75vw, 18px);
  position: absolute;
  right: auto;
  left: auto;
  width: 100%;
  bottom: 21px;
  transform: translateY(100%);
  transition-duration: 300ms;
}

.TextArea:hover{
  bottom: 0px;
  transform: translateY(0%);
}

</style>