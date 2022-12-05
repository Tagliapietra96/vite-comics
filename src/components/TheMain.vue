<template>
    <main>
        <Content :comics-list="comicsList"></Content>
        <ProductsBanner></ProductsBanner>
    </main>
</template>



<script>
import Content from './Content.vue';
import ProductsBanner from './ProductsBanner.vue';
export default {
    components: { Content, ProductsBanner },
    props: {
        comicsList: Array,
    },
}
</script>



<style scoped lang="scss">
main {
    padding-top: 105px;
}
</style>