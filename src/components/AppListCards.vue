<script>
    import AppCard from './AppCard.vue';

    export default {
        name: 'CardList',
        components: {
            AppCard
        }
    }
</script>

<template>
    <div>
        <div class="p-3 bg-black">Found X cards:</div>
        <AppCard/>
    </div>
</template>

<style lang="scss" scoped>
   
</style>