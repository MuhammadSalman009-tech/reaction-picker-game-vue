<template>
  <div class="block" v-if="showBlock" @click="stopTimer">
      click me
  </div>
</template>

<script>
export default {
    props:["delay"],
    data(){
        return{
            showBlock:false,
            timer:null,
            reactionTime:0
        }
    },
    mounted(){
        console.log("block component is rendered");
        setTimeout(() => {
            this.showBlock=true
            this.startTimer()
        }, this.delay);
        },
    methods:{
        startTimer(){
            this.timer=setInterval(() => {
                this.reactionTime+=10
            }, 10);
        },
        stopTimer(){
            clearInterval(this.timer);
            console.log(this.reactionTime);
        }
    }
}
</script>

<style>
.block{
    background-color: seagreen;
    color: #fff;
    width: 400px;
    margin: 40px auto;
    padding: 100px;
    border-radius: 20px;
}
</style>