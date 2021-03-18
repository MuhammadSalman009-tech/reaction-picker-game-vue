<template>
  <div class="results">
    <p>Reaction Time: {{score}}ms</p>
    <h2>{{rank}}</h2>
  </div>
</template>

<script>
export default {
    data(){
        return{
            rank:null
        }
    },
    props:["score"],
    mounted(){
    if(this.score<250){
        this.rank="1st Rank"
    }else if(this.score<500){
        this.rank="2nd Rank"
    }else{
        this.rank="3rd Rank"
    }
}
}
</script>

<style>
.results h2{
    color: seagreen;
}
</style>