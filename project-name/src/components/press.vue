<template>
    <div class="press">
        <div class="title">
            <div class="left">
               <h1>最新新闻</h1> 
            </div>
            <div class="right">查看全部</div>
        </div>
        <div class="con">
            <div class="con_left">
                <div class="con_left_top">
                    <img :src="dataImg">
                </div>
                <div class="con_left_bottom">
                    <div class="con_left_left">03-27
                        <p>2020</p>
                    </div>
                    <div class="con_left_right">
                        <div class="con_left_right_top">
                            <h3>{{dataTop}}</h3>
                            </div>
                        <div class="con_left_right_bottom">{{dataBot}}</div>
                    </div>
                </div>
            </div>
            <div class="con_right">
                <div class="con_right_flex">
                   <div class="con_right_left">
                       <h3>03-27</h3>
                       <p>2020</p>
                   </div>
                   <div class="con_right_right">
                       <div class="con_right_right_top">
                            <h3>{{dataTop}}</h3>
                            </div>
                        <div class="con_right_right_bottom">{{dataBot}}</div>
                   </div>
                </div>
         <div class="con_right_flex">
                   <div class="con_right_left">
                       <h3>03-27</h3>
                       <p>2020</p>
                   </div>
                   <div class="con_right_right">
                       <div class="con_right_right_top">
                            <h3>{{dataTop}}</h3>
                            </div>
                        <div class="con_right_right_bottom">{{dataBot}}</div>
                   </div>
                </div><div class="con_right_flex">
                   <div class="con_right_left">
                       <h3>03-27</h3>
                       <p>2020</p>
                   </div>
                   <div class="con_right_right">
                       <div class="con_right_right_top">
                            <h3>{{dataTop}}</h3>
                            </div>
                        <div class="con_right_right_bottom">{{dataBot}}</div>
                   </div>
                </div>
                
            </div>
        </div>
    </div>
</template>
<script>
import a from '../assets/1585033378524306.jpg'
export default {
    name:"Press",
    data:function(){
        return {
            dataImg:a,
            dataTop:"一砖一瓦春季线上招聘会来啦",
            dataBot:"一砖一瓦2020年第一届春季线上招聘会来啦，即日起至2020年3月28日可陆续报名，开幕时间为2020年3月28日"
        }
    }
}
</script>
<style scoped>
.press {
    margin-top: 50px;
    margin-bottom: 50px;
}
    .title {
        display: flex;
        width: 100%;
        justify-content: center;
    }
    .left {
        width: 40%;
        transition:all 0.5s ;
    }
    .left h1{
        padding-left: 10px;
        border-left: 3px solid red;
    }
    .left:hover {
        transform: translateX(10px);
        cursor: pointer;
    }
    .right {
        width: 40%;
        text-align: right;
    }
    .con{
         display: flex;
        width: 100%;
        justify-content: center;
        margin-top: 20px;
    }
    .con_left {
         width: 40%;
    }
    .con_left img {
        width: 95%;
        transition:all 0.5s ;
    } 
    .con_left img:hover {
        width: 100%;
    }
    .con_right {
         width: 40%;
    }
    .con_right_flex {
        display: flex;
        /* width: 100%; */
        height: 170px;
    }
    .con_left_bottom {
        display: flex;
        margin-top: 10px;
        justify-content: space-between;
    }
    .con_left_left {
        width: 20%;
        font-size: 30px;
        text-align: center;
    }
    .con_left_left p {
        color: lightgray;
    }

    .con_left_right {
        width: 80%;
        padding-left: 10px;
        border-left: 1px solid lightgray;
    }
    .con_left_right_top {
        color: dimgrey;
        transition:all 0.5s ;
    }
    .con_left_right_bottom {
        width: 95%;
        margin-top: 10px;
        font-size: 15px;
        color: darkgrey;
    }
    .con_left_right_top:hover {
        transform: translateX(10px);
        cursor: pointer;
    }
    .con_right_left {
        width: 20%;
        text-align: center;
    }
    .con_right_left h3 {
        font-size: 25px;
    }
    .con_right_left p {
         margin-top: 10px;
        font-size: 30px;
        color: darkgrey;
    }
    .con_right_right {
         width: 80%;
         height: 100px;
        padding-left: 10px;
        border-left: 1px solid lightgray;
    }
     .con_right_right_top {
        color: dimgrey;
        transition:all 0.5s ;
    }
    .con_right_right_bottom {
        width: 95%;
        margin-top: 30px;
        font-size: 15px;
        color: darkgrey;
    }
    .con_right_right_top:hover {
        transform: translateX(10px);
        cursor: pointer;
    }
</style>