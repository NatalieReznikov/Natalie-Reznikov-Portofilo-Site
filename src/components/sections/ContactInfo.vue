<template>
    <div id="ContactInfo">
        <h1>
            Natalie Reznikov
        </h1>
        <h5> 
            Teaching office: McConnell Engineering Building <br>
            Research lab: 141 du Président-Kennedy Avenue, 5th floor <br>
            Email: <a href="mailto:natalie.reznikov at mcgill.ca">natalie.reznikov at mcgill.ca</a>
        </h5>
        <div id="jacobCredit">
        <h3>
            Jacob Reznikov - Web Development, Web Design
        </h3>
        <h5> 
            Github: <a href="https://github.com/yakking">https://github.com/yakking</a> <br>
            Email: <a href="mailto:yakov.reznikov@mail.mcgill.ca">yakov.reznikov at mail.mcgill.ca</a> 
        </h5>
        </div>
        <div id="jennyCredit">
        <h3>
            Jenny Xu - Extra Coding Help
        </h3>
        <h5> 
            Github: <a href="https://github.com/jxu0053">https://github.com/jxu0053</a> <br>
            Email: <a href="mailto:yakov.reznikov@mail.mcgill.ca">jenny.xu at mail.mcgill.ca</a> 
        </h5>
        </div>
    </div>
</template>

<script>
export default {
name: "ContactInfo",

}
</script>

<style scoped>
#ContactInfo{
    position: relative;
    height: 100%;
    padding: 50px;
}

h1{
    margin: 50px;
}

#jacobCredit,#jennyCredit{
    display: block;
    position: absolute;
    width: fit-content;
    bottom: 50px;
    margin: 0px;
    padding: 0px;
}

#jacobCredit{
    left: 50px;
    right: auto;
}

#jennyCredit{
    left: auto;
    right: 50px;
}


</style>