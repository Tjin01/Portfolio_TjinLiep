<template>
    <div class="home_page_gallery">
     <div v-for="item in categories" 
        class="tech_topics"
        :key="item.photo" 
        v-bind:class="{tech_photo1: item.active}" 
        v-bind:style="{
        backgroundImage: 'url('+ item.photo +')'}"
        @mouseover="item.barActive = true" @mouseout="item.barActive = false"
         >
        <div class="hover_tech_topics" v-bind:class="{active: item.barActive}">
            <h4>{{item.topic}}</h4>
        </div>
     </div>
    </div>
</template>

<script>
import photo1 from '../../media/images/homepage4.jpg';
import photo2 from '../../media/images/homepage5.jpg';
import photo3 from '../../media/images/homepage6.jpg';
import photo4 from '../../media/images/homepage7.jpg';


export default {
    name: 'homegallery',
    data(){
        return{
            categories: [
                {photo: photo1, barActive: false, active: true, topic: 'Mac book'},
                {photo: photo2, barActive: false, active: true, topic: 'Idea' },
                {photo: photo3, barActive: false, active: true, topic: 'Matrix' },
                {photo: photo4, barActive: false, active: true, topic: 'Development'},
            ],
        }
    },
}
</script>

<style scoped>
.home_page_gallery{
    height: 100%;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
}

.home_page_gallery .tech_topics{
    flex: 1 0 22%;
    min-height: 320px;
    background-size: 500px;
    cursor: pointer;
    display: flex;
    position: relative;
}

.hover_tech_topics {
    width: 100%;
    height: 0;
    position: absolute;
    overflow: hidden;
    opacity: 0;
    bottom: 0;
    background: #ffff;
    text-align: center;
}

.tech_photo1 .active{
    overflow: auto;
    opacity: 0.9;
    height: 100px;
    transition: height 1s ease-in;
}

h4 {
  font-family: 'MuseoModerno', cursive;
  font-size: 1.2rem;
  text-transform: uppercase;
  letter-spacing: 3px;
}


/* Media Queries */

@media screen and (max-width: 768px){
.home_page_gallery{
    height: 100%;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
}

}



</style>