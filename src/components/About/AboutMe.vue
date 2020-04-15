<template>
    <div class="about_information"> 
        <h3> Profile </h3>
        <div class="about_profile_photo"> 
        <img src="../../media/images/donavan.jpeg">
        </div>
        <h4 class="stack_header" v-on:click="loadImage()"> Tech Stack <i class="fas fa-cubes"></i></h4>
        <div class="information">
            <p> Donavan Tjin Liep Shie </p>
            <p> Front-end developer </p>
        </div>
        <div class="tech_photo"> 
        <img src="" id="display_image">
        </div>
        <div class="familiar_with_tech">
            <div v-for="item in techstack" :key="item.name">
              <i :class="item.icon"></i> {{item.name}}
            </div>
        </div>
        <div class="skill_set">
            <div class="box1"><i class="far fa-smile-wink"></i></div>
            <div class="box2"><i class="far fa-smile"></i></div>
            <div class="box3"><i class="far fa-smile-beam"></i></div>
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
            changeimage: ''
        }
    },
    methods: {
        loadImage() {
         let self = this;
         for(let i = 0; i<self.techstack.length; i++){
            setTimeout(function() {
            document.getElementById('display_image').src = self.techstack[i].image
        },i*2000)
      }
     }
    }
}
</script>

<style scoped>
.about_information {
    position: relative;
    display: flex;
    height: 500px;
}

.about_information h3 {
    font-family: 'Bangers', cursive;
    letter-spacing: 4px;
    margin: 10px;
}

.about_profile_photo img {
    width: 130px;
    border-radius: 5px;
    position: absolute;
    top: 50px;
    left: 20px;
}
.stack_header {
    top: 220px;
    left: 550px;
    position: absolute;
    font-size: 1.2rem;
    font-family: 'Bangers', cursive;
    letter-spacing: 2px;
    cursor: pointer;
}

.familiar_with_tech {
    border-bottom: 1px groove white;
    border-top: 1px groove white;
    width: 40%;
    position: absolute;
    top: 250px;
    left: 350px;
    padding: 20px 0px 20px 0px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    text-align: center;
}

.familiar_with_tech div {
    background: gray;
    opacity: 0.8;
    margin: 5px;
    padding-top: 4px;
    width: 80%;
    border-radius: 5px;
    font-weight: 500;
    font-size: 0.9rem;
    height: 30px;
    letter-spacing: 2px;
    font-family: 'Cutive Mono', monospace;
    font-weight: 700;
}

.information{
    position: absolute;
    top: 200px;
    left: 20px;
}

.information p {
    font-family: 'Bangers', cursive;
    letter-spacing: 2px;
    font-size: 1.1rem;
    border-bottom: 1px groove white;
    border-radius: 2px;
}

.tech_photo img {
    width: 150px;
    position: absolute;
    top: 50px;
    left: 550px;
    border-radius: 4px;
}

.skill_set {
    display: flex;
    border-bottom: 1px solid rgb(58, 58, 58, 0.2);
    position: relative;
    top: 375px;
    left: 200px;
    width: 700px;
    height: 120px;
    border-radius: 4px;
    background: #fff;
    flex-direction: row;
    justify-content: center;
}

.box1, .box2, .box3 {
    width: 80px;
    height: 60px;
    border: 1px solid rgba(75, 75, 75, 0.87);
    margin: 30px;
    border-radius: 2px;
    transform: rotate(90deg);
    border-radius: 300px;
    text-align: center;
}

.box1 i , .box2 i, .box3 i {
    font-size: 2.5rem;
    margin: 10px;
    background: rgb(247, 247, 144);
    border-radius: 20px;;
}


.box1, .box2, .box3 {
    animation: boxshow 6s;
    animation-iteration-count: infinite;
}

@keyframes boxshow {
    0% {
      transform: rotate(110deg);
    }
    25% {
      transform: rotate(120deg);
    }
    50% {
      transform: rotate(140deg);
    }
    75% {
       transform: rotate(180deg)
    }
}


.fa-node-js{
    color: green;
}

.fa-js {
    color: yellow;
}

.fa-grav {
    color: rgb(158, 14, 158);
    opacity: 0.6;
}

.fa-vuejs {
    color: rgb(99, 235, 99);
}

.fa-css3-alt {
    color: rgba(117, 165, 255, 0.952);
}
.fa-database{
    color: rgb(47, 233, 47);
}
/* Media Queries */
@media screen and (min-width: 701px) and (max-width: 800px){
.skill_set {
    top: 375px;
    left: 140px;
    width: 500px;
}

.stack_header {
    top: 220px;
    left: 450px;
}

.tech_photo img {
    width: 150px;
    top: 50px;
    left: 450px;
}


.familiar_with_tech {
    border-bottom: 1px groove white;
    border-top: 1px groove white;
    width: 40%;
    position: absolute;
    top: 250px;
    left: 350px;
    padding: 20px 0px 20px 0px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    text-align: center;
}

.familiar_with_tech div {
    background: gray;
    width: 128px;
    font-size: 0.9em;
}
}
/* Media Queries Mobile */
@media screen and (max-width: 700px){
.about_information {
    height: 700px;
}

.familiar_with_tech {
    width: 200px;
    top: 290px;
    left: 60px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

.stack_header {
    top: 270px;
    left: 130px;
    font-size: 0.8em;
}

.familiar_with_tech div {
    width: 100px;
    font-size: 0.7em;
}

.tech_photo img {
    width: 100px;
    top: 50px;
    left: 180px;
}

.skill_set {
    top: 475px;
    left: 0;
    width: 150px;
    height: 100px;
}

.box1, .box2, .box3 {
    width: 80px;
    height: 60px;
    margin-top: 10px;
}

.box1 i , .box2 i, .box3 i {
    font-size: 1.9rem;
    margin: 10px;
}

}
</style>