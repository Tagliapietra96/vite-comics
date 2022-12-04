<template>
    <div>
        <div class="container">

        </div>
    </div>
</template>



<script>
export default {
    data() {
        return {
            dcComicsList: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News',
            ],
            shopList: [
                'Shop DC',
                'Shop DC Collections'
            ],
            dcList: [
                'Terms Of Use',
                'Privacy Policy (New)',
                'Ad Choices',
                ''
            ],
            sitesList: [

            ]
        }
    }
}
</script>



<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;

div {
    padding: $s-5;
}
</style>