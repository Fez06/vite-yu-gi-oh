<script>
    import AppCard from './AppCard.vue';
    import axios from 'axios';

    export default {
        name: 'CardList',
        components: {
            AppCard
        },
        data() {
            return {
                dataCards: []
            }
        },
        created() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=alien')
            .then((response)=> {
                console.log(response);
                this.dataCards = response.data;
            })
        }
    }
</script>

<template>
    <div>
        <div class="p-3 bg-black">Found X cards:</div>
        <AppCard v-for="card in dataCards"/>
    </div>
</template>

<style lang="scss" scoped>
   
</style>