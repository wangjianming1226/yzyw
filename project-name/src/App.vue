
<template>
    <div >
        <Header></Header>
        <Jdt></Jdt>
        <Business></Business>
        <Special></Special>
        <Press></Press>
        <Product></Product>
        <Footer></Footer>
    </div>
</template>

<script>
import Header from './components/header.vue'
import Jdt from './components/jdt.vue'
import Business from './components/business.vue'
import Special from './components/special.vue'
import Press from './components/press.vue'
import Product from './components/product.vue'
import Footer from './components/footer.vue'
export default {
    name:"App",
    components:{
        Header,
        Jdt,
        Business,
        Special,
        Press,
        Product,
        Footer
    }
}
</script>

<style >
    *{
        margin: 0;
        padding: 0;
    }
</style>