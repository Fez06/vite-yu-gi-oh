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
                this.dataCards = response.data.data;
                console.log(this.dataCards)
            })
        }
    }
</script>

<template>
    <div class="d-flex flex-wrap">
        <div class="p-3 bg-black w-100">Found X cards:</div>
        <div class="card-cont" v-for="(card, i) in dataCards">
            <AppCard :name='card.name'
                    :image="card.card_images.card.image_url"
            />
        </div>
        
    </div>
</template>

<style lang="scss" scoped>
    .card-cont{
        width: 20%;
    }
</style>