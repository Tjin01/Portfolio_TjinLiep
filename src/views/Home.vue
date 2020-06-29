<template>
    <div>
        <Homecontent> </Homecontent>
        <homegallery> </homegallery>
    </div>
</template>

<script>
import Homecontent from '../components/Home/Homecontent.vue';
import Homegallery from '../components/Home/Homecontent1.vue';

export default {
    name: 'home',
    components: {
      Homecontent,
      Homegallery
    }
}
</script>

<style scoped>

</style>