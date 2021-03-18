<template>
  <div class="block" v-if="showBlock">
      click me
  </div>
</template>

<script>
export default {
    props:["delay"],
    data(){
        return{
            showBlock:false
        }
    },
    mounted(){
        console.log("block component is rendered");
        setTimeout(() => {
            this.showBlock=true
        }, this.delay);
        },
    methods:{
        
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