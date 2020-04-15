<template>
    <div class="portfolio_projects">
        <div class="project_1">
            <h3> Saltbage </h3>
            <img src="../../media/images/neonpizza.jpg">
            <div class="tech_stack">
            <ul>
            <li><i class="fab fa-vuejs"></i> Vuejs</li>
            <li><i class="fas fa-database"></i> Mongodb </li>
            <li><i class="fas fa-server"></i> Express</li>
            <li><i class="fab fa-node-js"></i> Node</li>
            <li><i class="fab fa-grav"></i> Restfull Api</li>
            </ul>
            </div>
            <button type="button" v-on:click="saltBage"> Click Here </button>
        </div>
        <div class="project_2">
            <h3> Tjins cooking </h3>
            <img src="../../media/images/tjinscook.jpeg">
             <div class="tech_stack">
            <ul>
            <li><i class="fab fa-vuejs"></i> Vuejs</li>
            <li><i class="fas fa-database"></i> Mongodb </li>
            <li><i class="fas fa-server"></i> Express</li>
            <li><i class="fab fa-node-js"></i> Node</li>
            <li><i class="fab fa-grav"></i> GraphQL Api</li>
            </ul>
            </div>
            <button type="button" v-on:click="tjinCook">Click Here</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'portfoliocomponent',
    methods: {
        saltBage() {
            window.location.href = 'https://aqueous-oasis-88356.herokuapp.com/'
        },
        tjinCook() {
            window.location.href = 'https://cooktjin.herokuapp.com/'
        }
    }
}
</script>

<style scoped>
.portfolio_projects{
    font-family: 'Bangers', cursive;
    letter-spacing: 6px;
    display:flex;
    flex-direction: column;
    width: 100%;
}

.project_1 h3, 
.project_2 h3 {
    width: 15%;
    margin: 5px;
    font-size: 1.4em;
}

img {
    width: 20%;
    margin: 30px;
    cursor: pointer;
    border-radius: 5px;
    border: 1px groove white;
}

.project_1, 
.project_2 {
    position: relative;
    border-bottom: 1px solid green;
    border-radius: 5px;
    padding: 20px;
    margin: 30px;
}

.project_1 .tech_stack, 
.project_2 .tech_stack {
    width: 30%;
    display: grid;
    grid-template-columns: 1fr 1fr / -1;
    position: absolute;
    top: 60px;
    left: 330px;
}

.tech_stack li {
    margin: 5px;
    border-bottom: 1px groove #fff;
    border-radius: 4px;
    font-size: 0.9em;
    list-style: none;
    background: #fff;
    transition: background 3s;
}

.tech_stack li i {
    margin: 5px;
}

.tech_stack li:hover {
    background: rgb(245, 209, 144);
    opacity: 0.8;
    transition: background ease-in 2s;
    -webkit-transition: background ease-in 2s;
}

.project_1 button,
.project_2 button {
    width: 13%;
    height: 30px;
    background: rgba(211, 209, 209, 0.527);
    font-size: 0.9em;
    cursor: pointer;
    font-family: 'Cutive Mono', monospace;
    border-radius: 5px;
    position: sticky;
    top: 270px;
    left: 60px;
    font-weight: bold;
}
/* Media Queries */
@media screen and (min-width: 701px) and (max-width: 1024px) {
    
}
/* Media Queries Mobile devices */
@media screen and (max-width: 700px) {

.project_1, .project_2{
    height: 500px;
}

img {
    width: 60%;
}
.project_1 .tech_stack, 
.project_2 .tech_stack {
    top: 240px;
    left: 130px;
}

.project_1 button,
.project_2 button {
    width: 99px;
    height: 30px;
    top: 250px;;
    left: 20px;
    font-weight: bold;
}
}


</style>