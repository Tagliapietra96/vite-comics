<template>
<TheHeader></TheHeader>
</template>


<script>
import TheHeader from './components/TheHeader.vue';
export default {
  components: {TheHeader}
}
</script>



<style lang="scss">
  @use './styles/general.scss' as *;
  @use './styles/partials/variables.scss' as *;
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body{
    font-family: Arial, Helvetica, sans-serif;
    font-size: $s-3;
  }
</style>
