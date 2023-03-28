<script>
    export default {
        name: 'card',
        props: {
            name: String,
            image: String,
            archetips: String
        }
    }
</script>

<template>
    <div class="card bg-warning bg-gradient mb-5">
        <img :src="image" alt="img card">
        <div class="info">
            <div>Nome: {{ name }}</div>
            <div>Archetipo: {{ archetips }}</div>
        </div>
    </div>
    
</template>

<style lang="scss" scoped>
    .card {
    
        img {
            margin: auto;
            width: 100%;
            height: auto;
        }

        .info {
            height: 100px;
            
            div {
                padding: 10px;
            }
        }
    }
</style>