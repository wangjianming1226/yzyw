<template>
<transition>
    <div class="box">
        <div class="title">公司业务</div>
        <div class="business">
        <div v-for="(value,index) in dataImg" v-bind:key="value" class="con">
            <img :src="dataImg[index]" >
            <p>{{dataContent[index]}}</p>
            <span class="span">{{dataWZ[index]}}</span>
        </div>
    </div>
    </div>
   
</transition>
</template>
<script>
import One from '../assets/1-1Z91G42K0B7.jpg'
import Two from '../assets/1-1Z91G42Q6133.jpg'
import Three from '../assets/1-1Z91G4244L02.jpg'
import Four from '../assets/1-1Z91G42640622.jpg'
export default {
    name:"Business",
    data:function(){
        return {
            isShow:false,
            data:"公司业务",
            dataImg:[One,Two,Three,Four],
            dataContent:["职业教育","在线教育","高教服务","人才服务"],
            dataIndex:0,
            dataWZ:["一砖一瓦专注研发课程，建立科学培训体系，全面提升从业人员的岗位胜任能力",
                    "建筑鱼网校是一砖一瓦旗下从事建筑人才服务的自助式网络学习平台",
                    "源助教是为高等教育提供专业、易用、实用的系列教育产品",
                    "建筑人才网致力于打造建筑行业“一站式”人才服务领先品牌"]
        }
    },
    methods:{
      
    }
}
</script>
<style scoped>
  .box {
        width: 100%;
        margin-top: 50px;
    }
    .title {
        width: 100%;
        font-size: 25px;
        text-align: center;
    }
    .business {
        display: flex;
        width: 100%;
        justify-content: center;
        margin-top: 50px;
    }
  
    .con {
        width: 265px;
        height: 490px;
        margin-right: 20px;
        text-align: center;
        transition:all 0.5s ;
    }
    .business p {
        font-size: 20px;
    }
    .business span {
        font-size: 10px;
    }
    .business img {
        width: 265px;
        height: 355px;
    }
    .con:hover {
        transform: translateY(-10px);
        cursor: pointer;
    }
    .span:hover {
        color:silver;
    }
</style>