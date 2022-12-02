<template>
<TheHeader></TheHeader>
<TheMain></TheMain>
</template>


<script>
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
export default {
  components: {TheHeader,TheMain}
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
