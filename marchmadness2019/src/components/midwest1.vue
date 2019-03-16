<template>
    <div class="component">
        <div v-for="(match, index) in matches" v-bind:key="index" class="match round1">
            <!--<div :class="'m'+index" class="match"> -->
            <p class="slot slot1">
                <span class="seed">{{index+1}}</span> {{match[0][0]}} <em class="score">{{match[0][1]}}</em>
            </p>
            <p class="slot slot2">
                <span class="seed">{{16-index}} </span><span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
            </p>
        </div>
        <div v-for="(match, index) in matches" v-bind:key="index" class="match round2">
            <!--<div :class="'m'+index" class="match"> -->
            <p class="slot slot1">
                <span class="seed">{{index+1}}</span> {{match[0][0]}} <em class="score">{{match[0][1]}}</em>
            </p>
            <p class="slot slot2">
                <span class="seed">{{16-index}} </span><span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
            </p>
        </div>
    </div>
</template>

<script>
    export default{
        props: {
            matches: {
                type:Array,
                default: 6,
            }
        },
        methods:{
            
        }
    }
</script>

<style scoped>
.match{
    width: 125px;
    border: 1px solid #444;
    padding: 0;
    position: relative;
    border-left: 0px;
    height: 40px;
    font-size: 12px;
    margin-top:10px;
}
.slot{
    margin: 0;
    position: absolute;
    left: 0;
    right: 0;
    padding: 0 4px;
}
.slot2{
    bottom: 0px;
}
.score{
    float: right
}

</style>
