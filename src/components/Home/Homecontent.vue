<template>
    <div class="home_content">
        <div class="my_name"> 
        <span v-for="(item, index) in splitText" :key="index">
            {{item}}
        </span>
        </div>
      <i class="fas fa-meteor" v-bind:class="{star_effect: effect}"></i>
      <h1 class="home_header" v-bind:class="{header_effect: effect}">Welcome to my portfolio page</h1>
    </div>
</template>

<script>
export default {
    name: 'homecomponent',
    mounted(){
        setTimeout(() => this.runEffect(), 1000);
    },
    data() {
        return {
            effect: false,
            name: 'Donavan',
        }
    },
    methods: {
        runEffect(){
            this.effect = true;
        }
    },
    computed: {
        splitText(){
          return this.name.split('');
        }
    }
}
</script>

<style scoped>
.home_content{
    position: relative;
    background: #f6f6f6;
    height: 100%;
    min-height: 600px;
    font-family: 'MuseoModerno', cursive;
}

.home_content .home_header {
    letter-spacing: 5px;
    font-size: 2.2em;
    position: absolute;
    top: 40%;
    left: 42%;
    text-transform: uppercase;
    transform: rotateX(-20deg) rotateY(20deg);
}

.header_effect{
    font-size: 1.2em !important;
    transition: font-size 2s linear;
}

.fa-meteor {
    font-size: 2.2rem;
    position: absolute;
    top: 10%;
    left: 20%;
    opacity: 0.0;
    transform: rotate(270deg)
}

.star_effect {
   top: 43%;
   left: 40%;
   opacity: 1;
   transform: rotate(230deg);
   transition: transform 8s, top 2s linear, left 3s linear;
}

.my_name{
    position: absolute;
    top: 27%;
    left: 40%;
}

span{
    font-size: 2.4rem;
}

span:nth-child(1)::before{
    content: 'D';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 9s ease-out;
}

span:nth-child(2)::before{
    content: 'o';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 8s ease-out;
}

span:nth-child(3)::before{
    content: 'n';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 7s ease-out;
}

span:nth-child(4)::before{
    content: 'a';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 6s ease-out;
}

span:nth-child(5)::before{
    content: 'v';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 5s ease-out;
}

span:nth-child(6)::before{
    content: 'a';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 4s ease-out;
}

span:nth-child(7)::before{
    content: 'n';
    color:  #BDC3C7;
    overflow: hidden;
    position: absolute;
    opacity: 0.0;
    transform: rotate(90deg);
    top: -55%;
    animation: change 3s ease-out;
}


/* Media Queries */
@media screen and (max-width: 768px){
.home_content{
    min-height: 400px;
}

.my_name{
    position: absolute;
    top: 27%;
    left: 30%;
}

span{
    font-size: 1.5rem;
}

.home_content .home_header {
    font-size: 1.2em;
}

.header_effect{
    font-size: 0.6em !important;
    transition: font-size 2s linear;
}

.star_effect {
   font-size: 1.2em;
   top: 43%;
   left: 35%;
}


}

@keyframes change {
    50% {
        transform: translateX(90deg);
    }
    to{
        transform: rotate(0deg);
        opacity: 1;
    }
}




</style>