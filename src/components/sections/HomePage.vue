<template>
  <div id="HomePage">
    <div class = "homepage">
      <h1> <i> <shift>Natalie </shift> Reznikov</i> </h1>
      <h2>An Engineer in the body of a Biologist </h2>
    </div>

    <div class = "pfp">
      <img src = "../../assets/natalie picture_nobg_bw.png">
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
  background-image: radial-gradient(circle at 75% 50%, rgba(0,0,0,0.95) 30%, rgba(0,0,0,0));
}

shift{
  margin-left: 13px;
  display: block;
  margin-bottom: 10px;
}

.pfp{
  position: absolute;
  left: 60%;

}
img{
  width: 550px;
  height: auto;
}


.homepage {
    position: absolute;
    left: 25%;
    top: 35%;
  }
  .homepage h1 {
    position: static;
    color: white;
    font-size: 60px;
    text-align: left;
  }
  .homepage h2 {
    position: relative;
    right: 50px;
    top: -10px;
    font-size: 35px;
  }

</style>