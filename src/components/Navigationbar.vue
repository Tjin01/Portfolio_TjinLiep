<template>
    <div class="navbar_portfolio">
       <nav>
           <ul> 
            <li><router-link to="/"> Home </router-link></li>
            <li><router-link to="/portfolio"> Portfolio </router-link></li>
            <li><router-link to="/about"> About </router-link></li>
           </ul>
       </nav>
    </div>
</template>

<script>

export default {
    name: 'navigationbar',
}
</script>

<style>
.navbar_portfolio{
    width: 100%;
    display: flex;
    height: 300px;
    margin: 0;
    background: url('../media/images/pexels-photo.jpg');
    background-repeat: round;
    background-size: 600px;
    border-bottom: 1px groove white;
    position: relative;
}

.navbar_portfolio nav {
    position: absolute;
    top: 0;
    left: 10px;
}

.navbar_portfolio li {
    list-style: none;
    font-size: 1.2rem;
    float: left;
    margin: 5px;
    letter-spacing: 4px;
    font-family: 'Bangers', cursive;
    cursor: pointer;
    font-weight: 600;
    color: #fff;
}

.navbar_portfolio a {
    text-decoration: none;
    color: inherit;
}

/* Media Queries */
@media screen and (max-width: 700px) {
    .navbar_portfolio{
     width: 100%;
     background: url('../media/images/pexels-photo.jpg');
     background-repeat: round;
     padding: 100px;
     border-bottom: none;
}

.navbar_portfolio li {
    list-style: none;
    font-size: 0.9rem;
    float: left;
    margin: 5px;
    letter-spacing: 4px;
    font-family: 'Bangers', cursive;
    cursor: pointer;
    font-weight: 600;
    color: #fff;
}
}

</style>