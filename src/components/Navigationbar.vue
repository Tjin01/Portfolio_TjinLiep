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
    height: 70px;
    margin: 0;
    border-bottom: 1px groove white;
    position: relative;
    background:#2f2a1a;
    justify-content: flex-end;
}

.navbar_portfolio nav {
    position: absolute;
    top: 20px;
    right: 180px;
}

.navbar_portfolio li {
    list-style: none;
    font-size: 1.2rem;
    float: left;
    margin: 10px;
    letter-spacing: 4px;
    font-family: 'Bangers', cursive;
    cursor: pointer;
    font-weight: 600;
    color: #fff;
    position: relative;
}

.navbar_portfolio li::before {
    content: '';
    position: absolute;
    top: 20px;
    border-bottom: 2px solid green;
    border-radius: 5px;
    width: 0%;
    transition: width 1s linear;
}

.navbar_portfolio li:hover:before {
    width: 100%;
    transition: width 1s linear;
}


.navbar_portfolio a {
    text-decoration: none;
    color: inherit;
}

/* Media Queries */

@media screen and (max-width: 675px) {

.navbar_portfolio nav {
    position: absolute;
    top: 20px;
    right: 20px;
}
}




</style>