<template>
    <div class="home_content">
        <div class="creative_picture">
            <img src="../../media/images/photo1.jpg"/>
        </div>
        <div class="social_media">
            <i class="fab fa-instagram" v-on:click="instaGramlink"></i>
            <i class="fab fa-linkedin" v-on:click="linkedInlinkg"></i>
        </div>
        <div class="profile_intro"> 
            <p>My name is <strong> Donavan Tjin Liep Shie </strong> I'm a selftaught webdeveloper.
            I'am based in Almere in the Netherlands. I love programming because I am able to use 
            my creativity to create beautifull (web)application 
            by using different technologies.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'homecomponent',
    methods: {
        instaGramlink() {
            window.location.href = 'https://www.instagram.com/tjinnn/'
        },
        linkedInlinkg() {
            window.location.href = 'https://www.linkedin.com/in/donavan-tjin-liep-shie/'
        }
    }
}
</script>

<style scoped>

.home_content{
    position: relative;
    display: flex;
    height: 600px;
}

.creative_picture img {
    width: 35%;
    border-radius: 5px;
    position: absolute;
    top: 80px;
    left: 20px;
    border-bottom: 1px groove white;
}

.social_media {
    position: absolute;
    top: 5px;
    left: 5px;
}

.social_media
.fa-instagram,
.fa-linkedin {
    font-size: 25px;
    cursor: pointer;
    margin: 5px;
}

.profile_intro{
    border-bottom: 1px groove white;
    position: absolute;
    top: 280px;
    width: 60%;
    left: 380px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    padding: 30px;
}

.profile_intro p {
    letter-spacing: 4px;
    font-size: 1.4rem;
    font-family: 'Bangers', cursive;
    margin: 10px;
    background: -webkit-linear-gradient(#333, #333, #eee 115%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* Media Queries desktop */
@media screen and (max-width: 1024px){
.profile_intro{
    top: 250px;
    width: 60%;
    left: 180px;
}

.profile_intro p {
    letter-spacing: 4px;
    font-size: 1.1rem;
}

}

/* Media Queries Mobile device */
@media screen and (max-width: 800px) {
.profile_intro{
    top: 180px;
    width: 70%;
    left: 100px;
}

.profile_intro p {
    letter-spacing: 4px;
    font-size: 0.7rem;
}
}
</style>