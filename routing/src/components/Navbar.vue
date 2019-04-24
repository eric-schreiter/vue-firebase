<template>
    <nav>
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link :to="{name: 'About'}">About</router-link></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name:'Navbar',
    data(){
        return {

        }
    }
}
</script>


<style scoped>
    ul {
        list-style-type: none;
        padding:0;
        display: flex;
        justify-content: center;
    }
    ul li a {
        color:rebeccapurple;
        font-size:2rem;
        text-decoration: none;
    }
</style>
