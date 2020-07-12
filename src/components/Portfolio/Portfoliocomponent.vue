<template>
    <div class="portfolio_projects">
      <div class="projects">
          <div class="project_1" v-for="item in data" :key="item.id">
              <div class="project_description">
                <h4> {{item.project}} </h4>
                <p>
                    {{item.background}}
                </p>
                <div class="author">
                <span>Developed <strong> by </strong></span> <span class="author_name">Donavan Tjin Liep Shie </span>
                </div> 
                <button class="visit_website" v-on:click="saltBage(item.link)"> Visit website </button>
                <div class="underline"></div>
              </div>
              <div class="project_images">
                  <img :src="item.image">
              </div>
          </div>
      </div>
    </div>
</template>

<script>
import image1 from '../../media/images/portfolio1.jpg';
import image2 from '../../media/images/portfolio2.jpg';
import image3 from '../../media/images/exchange.jpg';
import image4 from '../../media/images/giphyapp.jpg';


export default {
    name: 'portfoliocomponent',
    data(){
        return{
            data: [
                {background: 'With this web application you can order a pizza and buy a giftcard for someone you would like to share the pizza with. The web application name is called Saltbage with this application. You\'re able to order the best pizza in Amsterdam.',
                 developer:'Donavan Tjin Liep Shie',
                 project: 'Saltbage application',
                 link: 'https://aqueous-oasis-88356.herokuapp.com/',
                 id: 1,
                 image: image1}, 
                {background: 'This web application makes it easy for you to select a suggested foodmeal based on the foodcategory. The core of the application is to help people find the best recipe based on the foodcategory that they would like to eat.',
                 developer:'Donavan Tjin Liep Shie', 
                 project: 'Food application',
                 link: 'https://cooktjin.herokuapp.com/',
                 id: 2,
                 image: image2},
                {
                 background: 'Let\'s say you\'re in foreign country and you would like to know what the currency is. With this web application you are able to see what the currency is and exchange it with you\'re local currency based on where you are from.',
                 developer: 'Donavan Tjin Liep Shie',
                 project: 'Exchange application',
                 link: 'https://happy-keller-3ac408.netlify.app/',
                 id: 3,
                 image: image3},
                {
                  background: 'In this digital world now a days GIFS are indispensable when you want to have a laugh. GIFs help us accurately convey our thoughts and feelings when we\'re limited to virtual communication. This application helps you to search for a GIFS',
                  developer: 'Donavan Tjin Liep Shie',
                  project: 'Giphy application',
                  link: 'https://romantic-kowalevski-244d92.netlify.app/',
                  id: 4,
                  image: image4,
                },
            ],
        }
    },
    methods: {
        saltBage(item) {
           window.open(`${item}`);
        },
    }
}
</script>

<style scoped>
.portfolio_projects {
    margin-top: 50px;
}

.projects {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
}

.project_1{
    height: 300px;
    display: flex;
    flex-direction: row;
    font-family: 'MuseoModerno', cursive;
}

.project_description{
    flex: 1;
    position: relative;
    border-radius: 5px;
}

.project_description h4 {
    position: absolute;
    top: 23%;
    left: 15%;
    font-size: 1.6rem;
}

.project_description p {
    width: 70%; 
    font-weight: 600;
    position: absolute;
    top: 40%;
    left: 15%;
    text-align: left;
    border-radius: 2px;
    font-size: 0.8rem;
}

.project_description .author{
    position: absolute;
    top: 62%;
    left: 15%;
}

.project_description span {
    font-size: 0.6rem;
    font-weight: 800;
    margin: 2px;
}

.author_name{
    color:#ffa063;
    cursor: pointer;
}

.project_images {
    flex: 1;
    text-align: center;
}

.project_images img {
    width: 70%;
    max-width: 380px;
    height: 260px;
    border-radius: 2px;
    object-fit: cover;
}

.underline {
    position: absolute;
    top: 90%;
    left: 15%;
    border-bottom: .0625rem solid #e4e4e4;
    width: 60%;
}


.visit_website {
    line-height: 2.3;
    width: 150px;
    position: absolute;
    top: 75%;
    left: 20%;
    cursor: pointer;
    border-style: none;
    font-family: 'MuseoModerno', cursive;
    font-size: 12px;
    padding: 0.25rem;
    background: #ECF0F1;
}

.visit_website:hover{
    background: #76D7C4;
    transition: background 2s linear;
}


/* Media Queries */

@media screen and (max-width: 768px) {
.portfolio_projects {
    margin-top: 10px;
}

.project_1{
    flex-direction: column;
    font-family: 'MuseoModerno', cursive;
    height: 500px;
}


.project_description{
    flex: 1;
    position: relative;
    border-radius: 5px;
}

.project_images img {
    width: 70%;
    max-width: 280px;
    height: 220px;
}


.project_description h4 {
    top: 10%;
    left: 15%;
    font-size: 1.2rem;
}


.project_description p {
    width: 70%; 
    font-weight: 600;
    top: 22%;
    left: 15%;
    font-size: 0.7rem;
}


}


</style>