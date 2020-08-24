<template>
    <div class="SectionButton" @click="$emit('selected')">
        <div class="ButtonWrapper">
            <div class="SectionText">
                {{ msg }}
            </div>
            <transition name="fade">
                <div v-if="active" class="UnderlineBar">
                </div>
            </transition>

            
        </div>
    </div>
</template>

<script>
export default {
    name : "SectionButton",
    props : {
        msg : String,
        activeID : Number,
        id : Number
    },
    computed : {
        active : function () {
            return (this.activeID == this.id);
        }
    },
}
</script>

<style scoped>
.fade-enter-active{
    animation: myPopUp 0.25s;
}
.fade-leave-active{
    animation: myPopUp 0.25s reverse;
}

@keyframes myPopUp {
    0%{
        left: 50%;
        width: 0%;
    }
    100%{
        left: 0%;
        width: 100%;
    }
}

.ButtonWrapper{
    height: 42px;
}


.SectionButton{
    display: grid;
    place-items: center;
    margin: 10px;
}
.SectionText{
    height: 35px;
    margin: 0 0 5px 0;
}
.UnderlineBar{
    --MainColor: var(--main-accent);
    width: 100%;
    background-color: var(--MainColor);
    height: 3px;
    position: relative;
}
.EmptyUnderlineBar{
    width: 100%;
    height: 3px;
}
</style>