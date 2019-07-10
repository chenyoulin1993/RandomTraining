<template>
    <div>
        <h1>今天怎么练
        </h1>
        <div id="text">
        <h6>不知道今天想练什么动作</h6>
        <h6>让电脑帮你决定吧</h6>
        <p><strong>结果仅供参考</strong></p>
        </div>
        <div class='cardOne'>  
            <button v-on:click="cheastMove" class='mainBtn'>胸部肌群</button>
            <div class="showValue">
            <ul>
                <li v-for='value in cheastChoosed'>{{ value }}</li><br/>
            </ul>
            </div>
        </div> 

        </br></br></br>
         <div class='cardTwo'>  
            <button v-on:click="backMove" class='mainBtn'>背部肌群</button>
            <div class="showValue">
            <ul>
                <li v-for='value in backChoosed'>{{ value }}</li><br/>
            </ul>
            </div>
        </div>   

           </br></br></br>
         <div class='cardOne'>  
            <button v-on:click="legMove" class='mainBtn'>腿部肌群</button>
            <div class="showValue">
            <ul>
                <li v-for='value in legChoosed'>{{ value }}</li><br/>
            </ul>
            </div>
        </div> 

           </br></br></br>
         <div class='cardTwo'>  
            <button v-on:click="shouderMove" class='mainBtn'>肩部肌群</button>
            <div class="showValue">
            <ul>
                <li v-for='value in shouderChoosed'>{{ value }}</li><br/>
            </ul>
            </div>
        </div> 

           </br></br></br>
         <div class='cardOne'>  
            <button v-on:click="armMove" class='mainBtn'>二三头肌</button>
            <div class="showValue">
            <ul>
                <li v-for='value in armChoosed'>{{ value }}</li><br/>
            </ul>
            </div>
        </div> 
    </br></br></br>
    </div>
</template>

<script>
export default {
    
    name:'Cheast',
   
    data(){
        return{
        cheastChoosed:[],
        backChoosed:[],
        legChoosed:[],
        shouderChoosed:[],
        armChoosed:[],
        cheastTraining:[
            '哑铃飞鸟','杠铃卧推','机械式胸推','双杠曲臂撑','哑铃上斜卧推','哑铃卧推','蝴蝶机夹胸','龙门架绳索夹胸'
        ],
        backTraining:[
            '杠铃硬拉','引体向上','俯身划船','杠铃划船','绳索下拉','三角柄下拉','龙门架V绳直臂下拉','单臂划船'
        ],
        legTraining:[
            '杠铃深蹲','坐姿腿屈伸','箭步蹲','俯卧腿弯举','坐姿腿弯举','直腿硬拉','倒蹬机'
        ],
        shouderTraining:[
            '哑铃侧平举','直立划船','站姿绳索反向飞鸟','双杠曲臂撑','站姿前平举','颈后推举','耸肩','史密斯肩推'
        ],
        armTraining:[
            '哑铃弯举','仰卧杠铃臂屈伸','牧师椅杠铃弯举','哑铃集中式弯举','绳索下压','俯身哑铃臂屈伸','二十一礼炮','固定器械下压'
        ],
        }
        },
    methods:{
        cheastMove:function(){           
            this.cheastChoosed.splice(0);
            do  { 
                    var num1 = 0;
                    var num2 = 0;
                    var num3 = 0;               
                    num1 += Math.floor((Math.random()*this.cheastTraining.length)+0);
                    num2 += Math.floor((Math.random()*this.cheastTraining.length)+0);
                    num3 += Math.floor((Math.random()*this.cheastTraining.length)+0);
            }
            while( num1 == num2 || num2 == num3 || num1 == num3);
            this.cheastChoosed.push(this.cheastTraining[num1]);
            this.cheastChoosed.push(this.cheastTraining[num2]);
            this.cheastChoosed.push(this.cheastTraining[num3]);
        },
        backMove:function(){           
            this.backChoosed.splice(0);
            do  { 
                    var num1 = 0;
                    var num2 = 0;
                    var num3 = 0;               
                    num1 += Math.floor((Math.random()*this.backTraining.length)+0);
                    num2 += Math.floor((Math.random()*this.backTraining.length)+0);
                    num3 += Math.floor((Math.random()*this.backTraining.length)+0);
            }
            while( num1 == num2 || num2 == num3 || num1 == num3);
            this.backChoosed.push(this.backTraining[num1]);
            this.backChoosed.push(this.backTraining[num2]);
            this.backChoosed.push(this.backTraining[num3]);
        },
        legMove:function(){           
            this.legChoosed.splice(0);
            do  { 
                    var num1 = 0;
                    var num2 = 0;
                    var num3 = 0;               
                    num1 += Math.floor((Math.random()*this.legTraining.length)+0);
                    num2 += Math.floor((Math.random()*this.legTraining.length)+0);
                    num3 += Math.floor((Math.random()*this.legTraining.length)+0);
            }
            while( num1 == num2 || num2 == num3 || num1 == num3);
            this.legChoosed.push(this.legTraining[num1]);
            this.legChoosed.push(this.legTraining[num2]);
            this.legChoosed.push(this.legTraining[num3]);
        },
        shouderMove:function(){           
            this.shouderChoosed.splice(0);
            do  { 
                    var num1 = 0;
                    var num2 = 0;
                    var num3 = 0;               
                    num1 += Math.floor((Math.random()*this.shouderTraining.length)+0);
                    num2 += Math.floor((Math.random()*this.shouderTraining.length)+0);
                    num3 += Math.floor((Math.random()*this.shouderTraining.length)+0);
            }
            while( num1 == num2 || num2 == num3 || num1 == num3);
            this.shouderChoosed.push(this.shouderTraining[num1]);
            this.shouderChoosed.push(this.shouderTraining[num2]);
            this.shouderChoosed.push(this.shouderTraining[num3]);
        },
        armMove:function(){           
            this.armChoosed.splice(0);
            do  { 
                    var num1 = 0;
                    var num2 = 0;
                    var num3 = 0;               
                    num1 += Math.floor((Math.random()*this.armTraining.length)+0);
                    num2 += Math.floor((Math.random()*this.armTraining.length)+0);
                    num3 += Math.floor((Math.random()*this.armTraining.length)+0);
            }
            while( num1 == num2 || num2 == num3 || num1 == num3);
            this.armChoosed.push(this.armTraining[num1]);
            this.armChoosed.push(this.armTraining[num2]);
            this.armChoosed.push(this.armTraining[num3]);
        }
    }
 }


</script>

<style scoped>



ul,li{ padding:0;margin:0;list-style:none}

#txt{
    margin: 3%;
}

li{
    margin:15%;
    
}


.mainBtn{
    color: #fff;
    background-color: #2d8cf0;
    border-color: #2d8cf0;
    padding: 6px 15px;
    font-size: 14px;
    border-radius: 4px;
    outline: 0;
    vertical-align: middle;
    line-height: 1.5;
    margin:5%;
}

.cardOne{
    color: azure;
    width: 250px;
    height: 300px;
    background-color: #baccd9;
    display: inline-grid;
    border-radius: 10px;
    
}
.cardTwo{
    color: azure;
    width: 250px;
    height: 300px;
    background-color: #619ac3;
    display: inline-grid;
    border-radius: 10px;
    
}
.showValue{
   
    width: 250px;
    height:222px;
    display: inline-grid;
    
}

</style>
