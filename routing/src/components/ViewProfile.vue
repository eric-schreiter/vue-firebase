<template>
    <div class="view-profile">
        <h1>Profile for {{ userId }}</h1>
    </div>
</template>

<script>
export default {
    name: 'ViewProfile',
    data(){
        return {
            userId: this.$route.params.user_id
        } 
    }
}
</script>

<style>
    
</style>
