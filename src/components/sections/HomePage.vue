<template>
  <div id="HomePage">
    <div class="homepage">
      <img src="./../../assets/home page v3 with E.png"/>
    </div>
    <svg @click="$emit('go-next')" height="150" viewBox="0 0 21 21" width="50" xmlns="http://www.w3.org/2000/svg"><path d="m.5 8.5 4-14-4-14" fill="none" stroke="#6FEB95" stroke-linecap="round" stroke-linejoin="round" transform="translate(9 15)"/></svg>

  </div>
</template>

<script>


export default {
  name : "HomePage"
}
</script>

<style scoped>
#HomePage{
  width: 100%;
  height: 100%;
  position: relative;
  display: block;
  background-image: radial-gradient(circle at 75% 50%, rgba(0,0,0,0.95) 30%, rgba(0,0,0,0));
}

.homepage{
  position: absolute;
  display: inline-block;
  top: 50%;
  left: 50%;
  width:80%;
  transform: translate3d(-50%,-50%,0);
}

img{
  display:inline-block;
  width: 100%;
  height: 100%;
}
svg{
  position: absolute;
  top: 50%;
  right: 0px;
  display: inline-block;
  transform: translate3D(0, -50%,0);
  transition: transform 0.3s;
}

svg:hover{
  transform: translate3D(-10px, -50%, 0);
}



</style>