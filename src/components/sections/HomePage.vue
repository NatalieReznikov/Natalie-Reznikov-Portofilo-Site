<template>
  <div id="HomePage">
    <div class="homepage">
      <img src="./../../assets/home page v3 with E.png"/>
    </div>
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
  width: 100%;
  height: 100%;
}

</style>