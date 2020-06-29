<template>
    <div class="tech_stack">
    <div class="stack"> 
       <div><h4>Vuejs</h4><i class="fab fa-vuejs"></i></div>
       <div><h4>Node</h4><i class="fas fa-server"></i></div>
       <div><h4>CSS</h4><i class="fab fa-css3-alt"></i></div>
       <div><h4>Javascript</h4><i class="fab fa-js"></i></div>
       <div><h4>Graphql</h4><i class="fas fa-user-astronaut"></i></div>
       <div><h4>Mongodb</h4><i class="fas fa-database"></i></div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'techstack',
    data() {
        return {
            techstack: [],
        }
    }
}
</script>

<style scoped>
.tech_stack{
    height: 100vh;
    margin-top:60px;
    max-height: 450px;
    position: relative;
} 
.stack {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 70%;
    max-width: 500px;
    position: absolute;
    top: 20%;
    left: 20%;
    font-family: 'MuseoModerno', cursive;
    text-align: center;
}

.stack div {
    border: 1px solid #D6DBDF;
    border-radius: 5px;
    margin: 10px;
    cursor:pointer;
}

.fa-vuejs,
.fa-server,
.fa-css3-alt,
.fa-js,
.fa-user-astronaut,
.fa-database {
    margin-top: 7px;
}

/* Odd number*/
.stack div:nth-child(1),.stack div:nth-child(3),.stack div:nth-child(5){
    height: 30px;
    flex: 1 0 30%;
    transition: flex 1s ease-out;
}

.stack div:nth-child(1):hover, div:nth-child(3):hover, div:nth-child(5):hover {
    flex: 1 0 35%;
    transition: background 1s ease-in, flex 1s ease-in;
    background: #F8C471;
}

/* Even */
.stack div:nth-child(2),.stack div:nth-child(4),.stack div:nth-child(6){
    height: 30px;
    flex: 1 0 30%;
    transition: flex 1s ease-out;
}

.stack div:nth-child(2):hover, div:nth-child(4):hover, div:nth-child(6):hover {
    background: #ABEBC6;
    flex: 1 0 35%;
    transition: background 1s ease-in, flex 1s ease-in;
}


/* Media Queries */

</style>