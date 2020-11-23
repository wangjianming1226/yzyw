<template>
<div class="footer">
        <ul>
            <li>
                <dt>一砖一瓦</dt>
                <dd>企业文化</dd>
                <dd>核心业务</dd>
                <dd>发展历程</dd>
                <dd>市场区域</dd>
                <dd>荣誉资质</dd>
                <dd>合作单位</dd>
            </li>
             <li>
                <dt>公司业务</dt>
                <dd>职业教育</dd>
                <dd>在线教育</dd>
                <dd>高教服务</dd>
                <dd>人才服务</dd>
            </li>
             <li>
                <dt>专题活动</dt>
                <dd>BIM专题</dd>
                <dd>造价专题</dd>
                <dd>总咨询师</dd>
                <dd>企业管理</dd>
                <dd>人才峰会</dd>
            </li>
              <li>
                <dt>新闻资讯</dt>
                <dd>公司新闻</dd>
                <dd>行业资讯</dd>
            </li>
             <li>
                 <dt>分支机构</dt>
                <dd>华北地区</dd>
                <dd>西南地区</dd>
                <dd>华中地区</dd>
                <dd>东北地区</dd>
                <dd>西北地区</dd>
                <dd>华南地区</dd>
            </li>
             <li>
                <dt>查询中心</dt>
                <dd>证书查询</dd>
            </li>
            <li>
               <p style="text-align:center;font-size:20px;">
                    全国统一服务热线<br>
                    400-998-4988
                </p> 
            </li>
        </ul>
        
    </div>
    
</template>
<script>
export default {
    name:"Footer"
}
</script>
<style scoped>
    .footer {
        display: flex;
        background: black;
        justify-content: center;
        padding-top: 30px;
        padding-bottom: 30px;
    }
    ul {
        list-style: none;
        cursor: pointer;
    }
    dt {
        color: white;
        margin-bottom: 10px;
    }
    dd {
        margin-bottom: 5px;
    }
    ul li {
        float: left;
        color: #BBBBAC;
        margin-right: 50px;
    }
    .bottom {
        color: #BBBBAC;
    }
</style>