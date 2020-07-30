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
  left: 57%;
  top: -15%;

}
img{
  width: 775px;
  height: auto;
}


.homepage {
    position: absolute;
    left: 23%;
    top: 28%;
  }
  .homepage h1 {
    position: static;
    color: white;
    font-size: 100px;
    text-align: left;
  }
  .homepage h2 {
    position: relative;
    right: 90px;
    top: -10px;
    font-size: 45px;
  }

</style>