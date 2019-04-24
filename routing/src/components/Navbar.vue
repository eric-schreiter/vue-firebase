<template>
    <nav>
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link :to="{name: 'About'}">About</router-link></li>
        </ul>
        <h2>User Profiles</h2>
        <ul>
            <li v-for="(id, index) in userIds" :key="index">
                <router-link :to="{name: 'ViewProfile', params:{user_id: id }}">
                    <span>Profile {{ id }}</span>
                </router-link>
            </li>
        </ul>
        <h2>Navigation Controls</h2>
        <ul>
            <li><button @click="goHome">Redirect to Home</button></li>
            <li><button @click="goBack">Go Back</button></li>
            <li><button @click="goForward">Go Forward</button></li>

        </ul>
    </nav>
</template>

<script>
export default {
    name:'Navbar',
    data(){
        return {
            userIds: ['1', '2','3','4']
        }
    },
    methods:{
        // page jumps 
        goHome(){
            this.$router.push({name: 'Home'},)
        },
        goBack(){
            this.$router.go(-1)
        },
        goForward(){
            this.$router.go(+1)
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
    a.router-link-exact-active {
        color:green;
    }
</style>
