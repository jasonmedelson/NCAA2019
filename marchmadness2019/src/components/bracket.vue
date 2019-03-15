<template>
    <div class="component">
        <div id="bracket">
            <div id="round1" class="round">
                <!-- start region1 -->
                <div class="region region1">
                    <h4 class="region1 first_region">
                        MIDWEST 
                    </h4>
                    <appMidWest :matches="matches"></appMidWest>
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
                    ["Maryland-Baltimore County", 77.73],
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
                    ["South Dakota State", 78.07],
                    ["North Carolina-Greensboro", 78.03],
                    ["San Diego State", 81.72],
                    ["Montana", 76.79],
                    ["Providence", 81.27],
                    ["Lipscomb", 72.45],
                    ["Pennsylvania", 75.55],
                    ["North Carolina State", 81.74],
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
                matches:[
                    
                ]
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
            }
        },
        mounted:function(){
            console.log("TEST")
            this.test();
        },
        components: {
            appMidWest: midwest,
        }
    }
</script>

<style scoped>
h4 {
    display: none;
    margin-block-start: 1.33em;
    margin-block-end: 1.33em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
    position: absolute;
    left: 170px;
    top: 165px;
    width: 150px;
}
</style>
