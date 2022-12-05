<template>
    <section class="bg-d">
        <div class="container">
            <h1 v-for="element in comicsList">{{element.series}}</h1>
        </div>
    </section>
</template>



<script>
export default {
    props:{
        comicsList: Array,
    }
}
</script>


<style scoped lang="scss">
@use '../styles/partials/variables' as *;

section{
    padding: 200px 0;
    h1{
        color:white;
    }
}
</style>