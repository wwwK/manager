<template>
  <router-view></router-view>
</template>

<script>
export default {
  name: "app",
  mounted(){
    let userInfo = this.$storage.getItem('userInfo');
    if(!userInfo)this.$router.push('/login')
  }
};
</script>

<style lang="scss">
@import "./assets/style/reset.css";
@import "./assets/style/index.scss";
</style>