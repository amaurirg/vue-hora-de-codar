<template>
<Banner />
  <div class="main-container">
    <h1>Monte seu burguer</h1>
    <BannerForm />
  </div>
</template>

<script>
import Banner from '../components/Banner.vue'
import BannerForm from '../components/BannerForm.vue'

export default {
    name: 'Home',
    components: {
        Banner,
        BannerForm
    }
};
</script>

<style scoped>
</style>