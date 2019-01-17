<template>
    <div>
        <AppHeader></AppHeader>
        <Content></Content>
        <Footer></Footer>
    </div>
</template>
<script>
import AppHeader from '@/components/AppHeader.vue'
import Content from '@/components/Content.vue'
import Footer from '@/components/Footer.vue'

export default { 
    name: 'Home',
    components: {
        AppHeader,
        Content,
        Footer
    }
}
</script>
<style>

</style>
  