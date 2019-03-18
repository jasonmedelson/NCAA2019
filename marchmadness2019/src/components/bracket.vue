<template>
    <div class="component">
        <div id="bracket" class="container-fluid">
            <div class="row justify-content-start">
                <div class="round-1-left mycol-1">
                    <div v-for="(match, index) in 8" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[matches[index][0][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index][0][3]}}</span> <span>{{matches[index][0][0]}}</span> <em class="score">{{matches[index][0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2" :class="[matches[index][1][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index][1][3]}} </span> <span>{{matches[index][1][0]}}</span> <em class="score">{{matches[index][1][1]}}</em>
                        </p>
                    </div>
                </div> 
                <div class="round-2-left mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in 4" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round2[index][0][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index][0][3]}}</span> <span>{{round2[index][0][0]}}</span> <em class="score">{{round2[index][0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2" :class="[round2[index][1][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index][1][3]}} </span> <span>{{round2[index][1][0]}}</span> <em class="score">{{round2[index][1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-3-left mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in 2" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round3[index][0][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index][0][3]}}</span> <span>{{round3[index][0][0]}}</span> <em class="score">{{round3[index][0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2" :class="[round3[index][1][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index][1][3]}} </span> <span>{{round3[index][1][0]}}</span> <em class="score">{{round3[index][1][1]}}</em>
                        </p>
                    </div>
                </div>   
                <div class="round-4-left mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in 1" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round4[index][0][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index][0][3]}}</span> <span>{{round4[index][0][0]}}</span> <em class="score">{{round4[index][0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2" :class="[round4[index][1][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index][1][3]}} </span> <span>{{round4[index][1][0]}}</span> <em class="score">{{round4[index][1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="center-seperator"></div>
                <div class="round-4-right right mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in 1" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round4[index+1][0][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index+1][0][3]}}</span> <span>{{round4[index+1][0][0]}}</span> <em class="score">{{round4[index+1][0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2" :class="[round4[index+1][1][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index+1][1][3]}} </span> <span>{{round4[index+1][1][0]}}</span> <em class="score">{{round4[index+1][1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="round-3-right right mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in 2" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round3[index+2][0][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index+2][0][3]}}</span> <span>{{round3[index+2][0][0]}}</span> <em class="score">{{round3[index+2][0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2" :class="[round3[index+2][1][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index+2][1][3]}} </span> <span>{{round3[index+2][1][0]}}</span> <em class="score">{{round3[index+2][1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-2-right right mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in 4" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round2[index+4][0][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index+4][0][3]}}</span> <span>{{round2[index+4][0][0]}}</span> <em class="score">{{round2[index+4][0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2" :class="[round2[index+4][1][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index+4][1][3]}} </span> <span>{{round2[index+4][1][0]}}</span> <em class="score">{{round2[index+4][1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-1-right right mycol-1">
                    <div v-for="(match, index) in 8" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[matches[index+8][0][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index+8][0][3]}}</span> <span>{{matches[index+8][0][0]}}</span> <em class="score">{{matches[index+8][0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2" :class="[matches[index+8][1][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index+8][1][3]}} </span> <span>{{matches[index+8][1][0]}}</span> <em class="score">{{matches[index+8][1][1]}}</em>
                        </p>
                    </div>
                </div> 
            </div>
            <div class="row justify-content-center final-four">
                <div class="round-3-left col-2 match round3 final-four-match">
                    <p class="slot slot1" :class="[round5[0][0][2]>4 ? 'win' : 'lose',{played:played5},{hideslot:!show5}]">
                        <span class="seed">{{round5[0][0][3]}}</span> <span>{{round5[0][0][0]}}</span> <em class="score">{{round5[0][0][1]}}</em>
                    </p>
                    <div class="spacer-3"></div>
                    <p class="slot slot2" :class="[round5[0][1][2]>4 ? 'win' : 'lose',{played:played5},{hideslot:!show5}]">
                        <span class="seed">{{round5[0][1][3]}}</span> <span>{{round5[0][1][0]}}</span> <em class="score">{{round5[0][1][1]}}</em>
                    </p>
                </div>  
                <div class="col-2 center px-0">
                    <div class="champ-top px-2">
                        <p style="padding-top:38px" :class="[round6[0][0][2]>5 ? 'win' : 'lose',{played:played6},{hideslot:!show6}]">
                            <span class="float-left"><span class="seed">{{round6[0][0][3]}}</span> <span>{{round6[0][0][0]}}</span> </span><em class="score">{{round6[0][0][1]}}</em>
                        </p>
                    </div>
                    <div class="championship ">
                        <div></div>
                    </div>
                    <div class="champ-bottom px-2">
                        <p style="padding-top:1px" :class="[round6[0][1][2]>5 ? 'win' : 'lose',{played:played6},{hideslot:!show6}]">
                            <span class="float-left"><span class="seed">{{round6[0][1][3]}}</span> <span>{{round6[0][1][0]}}</span> </span><em class="score">{{round6[0][1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="right col-2">
                    <div class="round-3-right  match round3 final-four-match">
                        <p class="slot slot1" :class="[round5[0][0][2]>4 ? 'win' : 'lose',{played:played5},{hideslot:!show5}]">
                            <span class="seed">{{round5[1][0][3]}}</span> <span>{{round5[1][0][0]}}</span> <em class="score">{{round5[1][0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2" :class="[round5[0][1][2]>4 ? 'win' : 'lose',{played:played5},{hideslot:!show5}]">
                            <span class="seed">{{round5[1][1][3]}} </span> <span>{{round5[1][1][0]}}</span> <em class="score">{{round5[1][1][1]}}</em>
                        </p>
                    </div>
                </div> 
            </div>
            <div class="row justify-content-start">
                <div class="round-1-left mycol-1">
                    <div v-for="(match, index) in 8" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[matches[index+16][0][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index+16][0][3]}}</span> <span>{{matches[index+16][0][0]}}</span> <em class="score">{{matches[index+16][0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2" :class="[matches[index+16][1][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index+16][1][3]}} </span> <span>{{matches[index+16][1][0]}}</span> <em class="score">{{matches[index+16][1][1]}}</em>
                        </p>
                    </div>
                </div> 
                <div class="round-2-left mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in 4" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round2[index+8][0][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index+8][0][3]}}</span> <span>{{round2[index+8][0][0]}}</span> <em class="score">{{round2[index+8][0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2" :class="[round2[index+8][1][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index+8][1][3]}} </span> <span>{{round2[index+8][1][0]}}</span> <em class="score">{{round2[index+8][1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-3-left mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in 2" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round3[index+4][0][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index+4][0][3]}}</span> <span>{{round3[index+4][0][0]}}</span> <em class="score">{{round3[index+4][0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2" :class="[round3[index+4][1][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index+4][1][3]}} </span> <span>{{round3[index+4][1][0]}}</span> <em class="score">{{round3[index+4][1][1]}}</em>
                        </p>
                    </div>
                </div>   
                <div class="round-4-left mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in 1" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round4[index+2][0][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index+2][0][3]}}</span> <span>{{round4[index+2][0][0]}}</span> <em class="score">{{round4[index+2][0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2" :class="[round4[index+2][1][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index+2][1][3]}} </span> <span>{{round4[index+2][1][0]}}</span> <em class="score">{{round4[index+2][1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="center-seperator"></div>
                <div class="round-4-right right mycol-1">
                    <div class="round-4-offset"></div>
                    <div v-for="(match, index) in 1" v-bind:key="index" class="match round4 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round4[index+3][0][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index+3][0][3]}}</span> <span>{{round4[index+3][0][0]}}</span> <em class="score">{{round4[index+3][0][1]}}</em>
                        </p>
                        <div class="spacer-4"></div>
                        <p class="slot slot2" :class="[round4[index+3][1][2]>3 ? 'win' : 'lose',{played:played4},{hideslot:!show4}]">
                            <span class="seed">{{round4[index+3][1][3]}} </span> <span>{{round4[index+3][1][0]}}</span> <em class="score">{{round4[index+3][1][1]}}</em>
                        </p>
                    </div>
                </div>
                <div class="round-3-right right mycol-1">
                    <div class="round-3-offset"></div>
                    <div v-for="(match, index) in 2" v-bind:key="index" class="match round3 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round3[index+6][0][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index+6][0][3]}}</span> <span>{{round3[index+6][0][0]}}</span> <em class="score">{{round3[index+6][0][1]}}</em>
                        </p>
                        <div class="spacer-3"></div>
                        <p class="slot slot2" :class="[round3[index+6][1][2]>2 ? 'win' : 'lose',{played:played3},{hideslot:!show3}]">
                            <span class="seed">{{round3[index+6][1][3]}} </span> <span>{{round3[index+6][1][0]}}</span> <em class="score">{{round3[index+6][1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-2-right right mycol-1">
                    <div class="round-2-offset"></div>
                    <div v-for="(match, index) in 4" v-bind:key="index" class="match round2 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[round2[index+12][0][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index+12][0][3]}}</span> <span>{{round2[index+12][0][0]}}</span> <em class="score">{{round2[index+12][0][1]}}</em>
                        </p>
                        <div class="spacer-2"></div>
                        <p class="slot slot2" :class="[round2[index+12][1][2]>1 ? 'win' : 'lose',{played:played2},{hideslot:!show2}]">
                            <span class="seed">{{round2[index+12][1][3]}} </span> <span>{{round2[index+12][1][0]}}</span> <em class="score">{{round2[index+12][1][1]}}</em>
                        </p>
                    </div>
                </div>  
                <div class="round-1-right right mycol-1">
                    <div v-for="(match, index) in 8" v-bind:key="index" class="match round1 row">
                        <!--<div :class="'m'+index" class="match"> -->
                        <p class="slot slot1" :class="[matches[index+24][0][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index+24][0][3]}}</span> <span>{{matches[index+24][0][0]}}</span> <em class="score">{{matches[index+24][0][1]}}</em>
                        </p>
                        <div class="spacer-1"></div>
                        <p class="slot slot2" :class="[matches[index+24][1][2]>0 ? 'win' : 'lose',{played:played1}]">
                            <span class="seed">{{matches[index+24][1][3]}} </span> <span>{{matches[index+24][1][0]}}</span> <em class="score">{{matches[index+24][1][1]}}</em>
                        </p>
                    </div>
                </div> 
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        data:function(){
            return{
                teams:[
                    ["Villanova", 97.66,0,1],
                    ["Michigan", 93.98,0,1],
                    ["Loyola (IL)", 87.27,0,1],
                    ["Kansas", 92.37,0,1],
                    ["Kansas State", 87.4,0,1],
                    ["Florida State", 87.48,0,1],
                    ["Duke", 94.56,0,1],
                    ["Texas Tech", 89.19,0,1],
                    ["Kentucky", 90.54,0,1],
                    ["Nevada", 84.49,0,1],
                    ["Gonzaga", 90.07,0,1],
                    ["Texas A&M", 88.13,0,1],
                    ["Clemson", 87.57,0,1],
                    ["Syracuse", 84.6,0,1],
                    ["West Virginia", 91.15,0,1],
                    ["Purdue", 89.95,0,1],
                    ["Maryland-Baltimore", 77.73,0,1],
                    ["Buffalo", 83.38,0,1],
                    ["Tennessee", 87.49,0,1],
                    ["Cincinnati", 91.21,0,1],
                    ["Xavier", 88.91,0,1],
                    ["Ohio State", 86.03,0,1],
                    ["Houston", 86.5,0,1],
                    ["North Carolina", 90.7,0,1],
                    ["Seton Hall", 85.95,0,1],
                    ["Auburn", 84.29,0,1],
                    ["Michigan State", 91.75,0,1],
                    ["Rhode Island", 83.75,0,1],
                    ["Alabama", 83.03,0,1],
                    ["Marshall", 77.86,0,1],
                    ["Florida", 87.22,0,1],
                    ["Butler", 85.96,0,1],
                    ["Virginia", 93.07,0,1],
                    ["Creighton", 83.4,0,1],
                    ["Davidson", 81.9,0,1],
                    ["Arizona", 87.86,0,1],
                    ["Miami (FL)", 83.94,0,1],
                    ["Wright State", 74.31,0,1],
                    ["Texas", 82.9,0,1],
                    ["Georgia State", 75.99,0,1],
                    ["Texas Southern", 69.4,0,1],
                    ["Missouri", 78.49,0,1],
                    ["South Dakota", 78.07,0,1],
                    ["North Carolina", 78.03,0,1],
                    ["San Diego State", 81.72,0,1],
                    ["Montana", 76.79,0,1],
                    ["Providence", 81.27,0,1],
                    ["Lipscomb", 72.45,0,1],
                    ["Pennsylvania", 75.55,0,1],
                    ["North Carolina", 81.74,0,1],
                    ["New Mexico State", 79.79,0,1],
                    ["College of Charleston", 76.44,0,1],
                    ["Texas Christian", 84.84,0,1],
                    ["Bucknell", 78.25,0,1],
                    ["Oklahoma", 82.1,0,1],
                    ["Iona", 74.79,0,1],
                    ["Radford", 71.64,0,1],
                    ["Virginia Tech", 83.43,0,1],
                    ["Murray State", 78.93,0,1],
                    ["Wichita State", 87.97,0,1],
                    ["St. Bonaventure", 81.37,0,1],
                    ["Stephen F. Austin", 74.78,0,1],
                    ["Arkansas", 83.29,0,1],
                    ["Cal State Fullerton", 71.8,0,1]
                ],
                matches:[],
                round2:[],
                round3:[],
                round4:[],
                round5:[],
                round6:[],
                played1:false,
                played2:false,
                played3:false,
                played4:false,
                played5:false,
                played6:false,
                show2:false,
                show3:false,
                show4:false,
                show5:false,
                show6:false,
                roundCount:0,
            }
        },
        props: {
            
        },
        methods:{
            test(){
                for(var i =0; i < 64; i=i+2){
                    var hold = [];
                    hold.push(this.teams[i],this.teams[i+1]);
                    this.matches.push(hold);
                }
            console.log(this.matches);
            },
            simFirstRound(){
                console.log("first")
                for(var i =0; i < 32; i=i+2){
                    var hold = [];
                    var win = Math.floor(Math.random() * 2);
                    var win2 = Math.floor(Math.random() * 2);
                    hold.push(this.matches[i][win],this.matches[i+1][win2]);
                    this.round2.push(hold)
                    if(win==0){
                        this.matches[i][0][2]++;
                    }
                    else{
                        this.matches[i][1][2]++;
                    }
                    if(win2==0){
                        this.matches[i+1][0][2]++;
                    }
                    else{
                        this.matches[i+1][1][2]++;
                    }
                    
                }
                console.log(this.round2)
            },
            simSecondRound(){
                console.log("second")
                for(var i =0; i < 16; i=i+2){
                    var hold = [];
                    var win = Math.floor(Math.random() * 2);
                    var win2 = Math.floor(Math.random() * 2);
                    hold.push(this.round2[i][win],this.round2[i+1][win2]);
                    this.round3.push(hold)
                    if(win==0){
                        this.round2[i][0][2]++;
                    }
                    else{
                        this.round2[i][1][2]++;
                    }
                    if(win2==0){
                        this.round2[i+1][0][2]++;
                    }
                    else{
                        this.round2[i+1][1][2]++;
                    }
                }
                console.log(this.round3) 
            },
            simThirdRound(){
                console.log("third")
                for(var i =0; i < 8; i=i+2){
                    var hold = [];
                    var win = Math.floor(Math.random() * 2);
                    var win2 = Math.floor(Math.random() * 2);
                    hold.push(this.round3[i][win],this.round3[i+1][win2]);
                    this.round4.push(hold)
                    if(win==0){
                        this.round3[i][0][2]++;
                    }
                    else{
                        this.round3[i][1][2]++;
                    }
                    if(win2==0){
                        this.round3[i+1][0][2]++;
                    }
                    else{
                        this.round3[i+1][1][2]++;
                    }
                }
                console.log(this.round4) 
            },
            simFourthRound(){
                console.log("fourth")
                for(var i =0; i < 4; i=i+2){
                    var hold = [];
                    var win = Math.floor(Math.random() * 2);
                    var win2 = Math.floor(Math.random() * 2);
                    hold.push(this.round4[i][win],this.round4[i+1][win2]);
                    this.round5.push(hold)
                    if(win==0){
                        this.round4[i][0][2]++;
                    }
                    else{
                        this.round4[i][1][2]++;
                    }
                    if(win2==0){
                        this.round4[i+1][0][2]++;
                    }
                    else{
                        this.round4[i+1][1][2]++;
                    }
                }
                console.log(this.round5) 
            },
            simFifthRound(){
                console.log("fifth")
                 var hold = [];
                    var win = Math.floor(Math.random() * 2);
                    var win2 = Math.floor(Math.random() * 2);
                    hold.push(this.round5[0][win],this.round5[1][win2]);
                    this.round6.push(hold)
                    if(win==0){
                        this.round5[0][0][2]++;
                    }
                    else{
                        this.round5[0][1][2]++;
                    }
                    if(win2==0){
                        this.round5[1][0][2]++;
                    }
                    else{
                        this.round5[1][1][2]++;
                    }
                console.log(this.round6) 
            },
            simSixRound(){
                console.log("six")
                 var hold = [];
                    var win = Math.floor(Math.random() * 2);
                    if(win==0){
                        this.round6[0][0][2]++;
                    }
                    else{
                        this.round6[0][1][2]++;
                    }
            },
            revealRound(){
                console.log("reveal")
                this.roundCount++;
                var round = this.roundCount;
                if(round>=1){
                    this.played1 = true;
                    this.show2 = true;
                }
                if(round>=2){
                    this.played2 = true;
                    this.show3 = true;
                }
                if(round>=3){
                    this.played3 = true;
                    this.show4 = true;
                }
                if(round>=4){
                    this.played4 = true;
                    this.show5 = true;
                }
                if(round>=5){
                    this.played5 = true;
                    this.show6 = true;
                }
                if(round>=6){
                    this.played6 = true;
                }

            },
            restore(){
                this.teams=[
                    ["Villanova", 97.66,0,1],
                    ["Michigan", 93.98,0,1],
                    ["Loyola (IL)", 87.27,0,1],
                    ["Kansas", 92.37,0,1],
                    ["Kansas State", 87.4,0,1],
                    ["Florida State", 87.48,0,1],
                    ["Duke", 94.56,0,1],
                    ["Texas Tech", 89.19,0,1],
                    ["Kentucky", 90.54,0,1],
                    ["Nevada", 84.49,0,1],
                    ["Gonzaga", 90.07,0,1],
                    ["Texas A&M", 88.13,0,1],
                    ["Clemson", 87.57,0,1],
                    ["Syracuse", 84.6,0,1],
                    ["West Virginia", 91.15,0,1],
                    ["Purdue", 89.95,0,1],
                    ["Maryland-Baltimore", 77.73,0,1],
                    ["Buffalo", 83.38,0,1],
                    ["Tennessee", 87.49,0,1],
                    ["Cincinnati", 91.21,0,1],
                    ["Xavier", 88.91,0,1],
                    ["Ohio State", 86.03,0,1],
                    ["Houston", 86.5,0,1],
                    ["North Carolina", 90.7,0,1],
                    ["Seton Hall", 85.95,0,1],
                    ["Auburn", 84.29,0,1],
                    ["Michigan State", 91.75,0,1],
                    ["Rhode Island", 83.75,0,1],
                    ["Alabama", 83.03,0,1],
                    ["Marshall", 77.86,0,1],
                    ["Florida", 87.22,0,1],
                    ["Butler", 85.96,0,1],
                    ["Virginia", 93.07,0,1],
                    ["Creighton", 83.4,0,1],
                    ["Davidson", 81.9,0,1],
                    ["Arizona", 87.86,0,1],
                    ["Miami (FL)", 83.94,0,1],
                    ["Wright State", 74.31,0,1],
                    ["Texas", 82.9,0,1],
                    ["Georgia State", 75.99,0,1],
                    ["Texas Southern", 69.4,0,1],
                    ["Missouri", 78.49,0,1],
                    ["South Dakota", 78.07,0,1],
                    ["North Carolina", 78.03,0,1],
                    ["San Diego State", 81.72,0,1],
                    ["Montana", 76.79,0,1],
                    ["Providence", 81.27,0,1],
                    ["Lipscomb", 72.45,0,1],
                    ["Pennsylvania", 75.55,0,1],
                    ["North Carolina", 81.74,0,1],
                    ["New Mexico State", 79.79,0,1],
                    ["College of Charleston", 76.44,0,1],
                    ["Texas Christian", 84.84,0,1],
                    ["Bucknell", 78.25,0,1],
                    ["Oklahoma", 82.1,0,1],
                    ["Iona", 74.79,0,1],
                    ["Radford", 71.64,0,1],
                    ["Virginia Tech", 83.43,0,1],
                    ["Murray State", 78.93,0,1],
                    ["Wichita State", 87.97,0,1],
                    ["St. Bonaventure", 81.37,0,1],
                    ["Stephen F. Austin", 74.78,0,1],
                    ["Arkansas", 83.29,0,1],
                    ["Cal State Fullerton", 71.8,0,1]
                ];
                this.matches=[];
                this.round2=[];
                this.round3=[];
                this.round4=[];
                this.round5=[];
                this.round6=[];
                this.played1=false;
                this.played2=false;
                this.played3=false;
                this.played4=false;
                this.played5=false;
                this.played6=false;
                this.show2=false;
                this.show3=false;
                this.show4=false;
                this.show5=false;
                this.show6=false;
                this.roundCount=0;
            },
            revealAll(){
                this.restore();
                this.roundCount = 7;
                this.test();
                this.simFirstRound();
                this.simSecondRound();
                this.simThirdRound();
                this.simFourthRound();
                this.simFifthRound();
                this.simSixRound();
                this.revealRound();
            },
            reset(){
                this.restore();
                this.test();
                this.simFirstRound();
                this.simSecondRound();
                this.simThirdRound();
                this.simFourthRound();
                this.simFifthRound();
                this.simSixRound();
            }
        },
        beforeMount:function(){
            console.log("TEST")
            this.test();
            this.simFirstRound();
            this.simSecondRound();
            this.simThirdRound();
            this.simFourthRound();
            this.simFifthRound();
            this.simSixRound();
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
.right.col-2{
    padding: 0px;
}
.final-four-match{
    margin-bottom:50px !important;
}
.championship{
    border: 0.5px solid #444;
}
.champ-top{
    height:55px;
    font-size: 12px;
}
.champ-bottom{
    font-size: 12px;
}
.win.played{
    font-weight: bold;
    color:lightskyblue;
}
.lose.played{
    text-decoration: line-through;
}
.lose.played span{
    text-decoration: line-through;
}
.hideslot{
    visibility: hidden;
}

</style>
