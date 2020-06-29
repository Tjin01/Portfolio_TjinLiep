<template>
    <div>
        <AboutMe> </AboutMe>
        <Techstack></Techstack>
    </div>
</template>

<script>
import AboutMe from '../components/About/AboutMe.vue';
import Techstack from '../components/About/Stack.vue';

export default {
    name: 'about',
    components: {
        AboutMe,
        Techstack
    }
}
</script>

<style scoped>

</style>