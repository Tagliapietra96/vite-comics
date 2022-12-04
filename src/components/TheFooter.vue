<template>
<footer>
<FooterLinks></FooterLinks>
<FooterNav></FooterNav>
</footer>
</template>



<script>
import FooterLinks from './FooterLinks.vue';
import FooterNav from './FooterNav.vue';
export default {
    components: {FooterLinks,FooterNav},
}
</script>



<style scoped lang="scss">
    footer{
        background-image: url('/img/footer-bg.jpg');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
</style>