<script>
    export default {
        name: 'card',
        props: {
            name: String,
            image: String
        }
    }
</script>

<template>
    <div class="card">
        <img :src="image" alt="img card">
        <div>nome: {{ name }}</div>
    </div>
    
</template>

<style lang="scss" scoped>
    .card {
        
        height: 140px;

        img {
            margin: auto;
        }
    }
</style>