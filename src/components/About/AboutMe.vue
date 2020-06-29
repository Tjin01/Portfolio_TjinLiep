<template>
    <div class="about_information">
        <div class="bio_information"> 
            <div class="bio_background">
                <h4>Building beautiful web applications is what I like to do</h4>
                <p>
                {{letterbyletter}}
                </p>
            </div>
            <div class="bio_background_second">
                <p>
                I have a Bachelor of Science degree and at the moment I’m working as a supply chain employee at the headquarters of the Lidl in the Netherlands.
                I am looking for an entry/junior level position to start my career as a front-end developer.
                My main goal is to become a full stack webdeveloper and built beautiful scalable applications. 
                In my spare time I like to go to the gym at least 3 times in a week. 
                </p>
            </div>
            <div class="bio_image">
                <img src="../../media/images/donavan.jpeg" @mouseover="effect = true" @mouseleave="effect = false">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'aboutcomponent',
    data() {
        return {
            techstack: [
                {name: 'Nodejs', icon: 'fab fa-node-js', image: require('../../media/images/node.jpg')},
                {name: 'Javascript', icon: 'fab fa-js', image: require('../../media/images/js.png')},
                {name: 'GraphQL', icon: 'fab fa-grav', image: require('../../media/images/graphql.png')},
                {name: 'Vuejs', icon: 'fab fa-vuejs', image: require('../../media/images/vuejs.png')},
                {name: 'CSS', icon: 'fab fa-css3-alt', image: require('../../media/images/css3.png')},
                {name: 'Mongodb', icon: 'fas fa-database', image: require('../../media/images/MongoDB.png')},
                ],
             letterbyletter: 'My name is Donavan Tjin Liep Shie. I\'am a selftaught webdeveloper. I\'am based in Almere in the Netherlands. I love programming because I am able to use  my creativity to create beautifull (web)application by using different technologies.',
             effect: false,
        }
    },
}
</script>

<style scoped>
.about_information{
    font-family: 'MuseoModerno', cursive;
}

.bio_information {
    position: relative;
    top: 50px;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin: 5px;
}

.bio_background h4, p {
    width: 100%;
    max-width: 450px;
}

.bio_background h4 {
    font-size: 1.7rem;
}

.bio_image {
    width: 300px;
    text-align: center;
    border-radius: 100px;
    outline: none;
}

.bio_image img {
    width: 100%;
    max-width: 200px;
    border-radius: 280px;
    height: 200px;
    margin: 5px;
    background-size: cover;
    cursor: pointer;
}

.bio_background_second {
    width: 70%;
    max-width: 450px;
}

.bio_background_second p {
    font-size: 0.9rem;
    text-align: left;
}

.effect_1 {
    opacity: 1;
    transition: opacity 2s linear;
    background: #FCFCFC;
}
/* Media Queries */
@media screen and (max-width: 768px){
.bio_information {
    flex-direction: column;
    top: 0px;
}

.bio_background {
    border-bottom: 1px solid #D5D8DC;
    margin: 10px;
}

.bio_background_second {
    width: 100%;
    margin: 10px;
}

.bio_background h4 {
    font-size: 1.2rem;
    font-weight: 900;
}

}
</style>