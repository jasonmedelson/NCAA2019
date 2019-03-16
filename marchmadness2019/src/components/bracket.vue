<template>
    <div class="component">
        <div id="bracket" class="container-fluid">
            <div class="row justify-content-start">
                <div class="round-1-left mycol-1">
                    <div v-for="(match, index) in matches" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div> 
                <div class="round-2-left mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in round2" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-3-left mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in round3" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>   
                <div class="round-4-left mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in round4" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="center-seperator"></div>
                <div class="round-4-right right mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in round4" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="round-3-right right mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in round3" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-2-right right mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in round2" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-1-right right mycol-1">
                    <div v-for="(match, index) in matches" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div> 
            </div>
            <div class="row final-four">
                <div class="round-3-left col-2">
                    <div v-for="(match, index) in round4" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>   
            </div>
            <div class="row justify-content-start">
                <div class="round-1-left mycol-1">
                    <div v-for="(match, index) in matches" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div> 
                <div class="round-2-left mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in round2" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-3-left mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in round3" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>   
                <div class="round-4-left mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in round4" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="center-seperator"></div>
                <div class="round-4-right right mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in round4" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="round-3-right right mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in round3" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-2-right right mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in round2" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-1-right right mycol-1">
                    <div v-for="(match, index) in matches" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1">
                            <span class="seed">{{index+1}}</span> <span>{{match[0][0]}}</span> <em class="score">{{match[0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2">
                            <span class="seed">{{16-index}} </span> <span>{{match[1][0]}}</span> <em class="score">{{match[1][1]}}</em>
                        </p>
                    </div>
                </div> 
            </div>
        </div>
    </div>
</template>

<script>
    import midwest from './midwest1.vue';
    export default{
        data:function(){
            return{
                teams:[
                    ["Villanova", 97.66],
                    ["Michigan", 93.98],
                    ["Loyola (IL)", 87.27],
                    ["Kansas", 92.37],
                    ["Kansas State", 87.4],
                    ["Florida State", 87.48],
                    ["Duke", 94.56],
                    ["Texas Tech", 89.19],
                    ["Kentucky", 90.54],
                    ["Nevada", 84.49],
                    ["Gonzaga", 90.07],
                    ["Texas A&M", 88.13],
                    ["Clemson", 87.57],
                    ["Syracuse", 84.6],
                    ["West Virginia", 91.15],
                    ["Purdue", 89.95],
                    ["Maryland-Baltimore", 77.73],
                    ["Buffalo", 83.38],
                    ["Tennessee", 87.49],
                    ["Cincinnati", 91.21],
                    ["Xavier", 88.91],
                    ["Ohio State", 86.03],
                    ["Houston", 86.5],
                    ["North Carolina", 90.7],
                    ["Seton Hall", 85.95],
                    ["Auburn", 84.29],
                    ["Michigan State", 91.75],
                    ["Rhode Island", 83.75],
                    ["Alabama", 83.03],
                    ["Marshall", 77.86],
                    ["Florida", 87.22],
                    ["Butler", 85.96],
                    ["Virginia", 93.07],
                    ["Creighton", 83.4],
                    ["Davidson", 81.9],
                    ["Arizona", 87.86],
                    ["Miami (FL)", 83.94],
                    ["Wright State", 74.31],
                    ["Texas", 82.9],
                    ["Georgia State", 75.99],
                    ["Texas Southern", 69.4],
                    ["Missouri", 78.49],
                    ["South Dakota", 78.07],
                    ["North Carolina", 78.03],
                    ["San Diego State", 81.72],
                    ["Montana", 76.79],
                    ["Providence", 81.27],
                    ["Lipscomb", 72.45],
                    ["Pennsylvania", 75.55],
                    ["North Carolina", 81.74],
                    ["New Mexico State", 79.79],
                    ["College of Charleston", 76.44],
                    ["Texas Christian", 84.84],
                    ["Bucknell", 78.25],
                    ["Oklahoma", 82.1],
                    ["Iona", 74.79],
                    ["Radford", 71.64],
                    ["Virginia Tech", 83.43],
                    ["Murray State", 78.93],
                    ["Wichita State", 87.97],
                    ["St. Bonaventure", 81.37],
                    ["Stephen F. Austin", 74.78],
                    ["Arkansas", 83.29],
                    ["Cal State Fullerton", 71.8]
                ],
                matches:[],
                round2:[],
                round3:[],
                round4:[],
                round5:[],
            }
        },
        props: {
            
        },
        methods:{
            test(){
                for(var i =0; i < 16; i=i+2){
                    var hold = [];
                    hold.push(this.teams[i],this.teams[i+1]);
                    this.matches.push(hold);
                }
            console.log(this.matches);
            },
            simFirstRound(){
                console.log("first")
                for(var i =0; i < 8; i=i+2){
                    var hold = [];
                    hold.push(this.matches[i][0],this.matches[i+1][0])
                    this.round2.push(hold)
                }
                console.log(this.round2)
            },
            simSecondRound(){
                console.log("second")
                for(var i =0; i < 4; i=i+2){
                    var hold = [];
                    hold.push(this.round2[i][0],this.round2[i+1][0])
                    this.round3.push(hold)
                }
                console.log(this.round3) 
            },
            simThirdRound(){
                console.log("third")
                for(var i =0; i < 2; i=i+2){
                    var hold = [];
                    hold.push(this.round3[i][0],this.round3[i+1][0])
                    this.round4.push(hold)
                }
                console.log(this.round4) 
            },
            simfourthRound(){
                console.log("fourth")
                for(var i =0; i < 2; i=i+2){
                    var hold = [];
                    hold.push(this.round4[i][0],this.round4[i][0])
                    this.round5.push(hold)
                }
                console.log(this.round5) 
            }
        },
        mounted:function(){
            console.log("TEST")
            this.test();
            this.simFirstRound();
            this.simSecondRound();
            this.simThirdRound();
            this.simfourthRound();
        },
        components: {
            appMidWest: midwest,
        }
    }
</script>

<style scoped>
.match{
    border: 1px solid #444;
    padding: 0;
    border-left: 0px;
    height: 40px;
    font-size: 12px;
    margin-top:10px;
    text-align: left;
    white-space: nowrap;
}
.right .match{
    border: 1px solid #444 !important;
    border-right: 0px !important;
}
.slot{
    margin-bottom: 5px;
    width: 100%;
    max-height: 20px;
    white-space: nowrap;
    overflow: hidden;
}
.score{
    float: right;
    padding-right:2px;
}
.mycol-1{
    width:12%;
    padding:15px;
}
.center-seperator{
    width:40px;
}
.round-2-offset{
    height:20px;
}
.round-3-offset{
    height:45px;
}
.round-4-offset{
    height:90px;
}
.match.round2{
    height:50px;
    margin-bottom:50px;
}
.match.round3{
    height:100px;
    margin-bottom:100px;
}
.match.round4{
    height:200px;
    margin-bottom:100px;
}
.spacer-2{
    height:10px;
    width:1px;
}
.spacer-3{
    height:60px;
    width:1px;
}
.spacer-4{
    height:160px;
    width:1px;
}
.round-1-right{
    float:right;
}
</style>
