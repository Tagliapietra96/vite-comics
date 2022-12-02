<template>
    <main>
        <Content></Content>
        <ProductsBanner></ProductsBanner>
    </main>
</template>



<script>
import Content from './Content.vue';
import ProductsBanner from './ProductsBanner.vue';
export default {
    components: { Content, ProductsBanner }
}
</script>



<style scoped lang="scss">
main {
    padding-top: 105px;
}
</style>