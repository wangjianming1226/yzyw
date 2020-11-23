<template>
<div>
<div class="product">
        <div class="title">
            {{title}}
        </div>
</div>
        <div class="img">
                <img v-for="(value,index) in dataImg" v-bind:key="value" :src="dataImg[index]">
        </div>
    </div>
</template>
<script>
import a from "../assets/jianzhuwangzhanlogo.png"
import b from "../assets/jianzhuyu.png"
import c from "../assets/yuanzhujiaologo.png"
import d from "../assets/yizhuanyiwalogo.png"
export default {
    name:"Product",
    data:function(){
        return {
            title:"旗下产品",
            dataImg:[a,b,c,d]
        }
    }
}
</script>
<style scoped>
div {
    padding-top: 30px;
    padding-bottom: 30px;
    background: #F6F6F6;
}
.product {
    display: flex;
    width: 100%;
    justify-content: center;
}
.title {
    transition:all 0.5s ;
    font-size: 30px;
    border-bottom: 1px solid red;
}
.img {
    display: flex;
    /* margin-top: 30px; */
    width: 100%;
    justify-content: center;
}
.img img {
    width: 165px;
    height: 46px;
    margin-right: 50px;
    transition:all 0.5s ;
}
.title:hover {
        transform: translateY(-10px);
        cursor: pointer;
    }
    .img img:hover {
        transform: translateY(-10px);
        cursor: pointer;
    }
</style>