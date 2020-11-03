<template>
  <div class="layout">
    <Header/>
    <nuxt />
    <Footer/>
  </div>
</template>

<script>
import Header from '~/components/common/Header';
import Footer from '~/components/common/Footer';
export default {
  components:{Footer, Header}
}
</script>

<style>
.layout {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>
