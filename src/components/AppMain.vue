<script>
    import AppListCardsVue from './AppListCards.vue';

    export default {
        name: 'main',
        components: {
            AppListCardsVue
        }
    }
</script>

<template>
    <div class="bg-warning bg-gradient">
        <div class="w-75 m-auto">
            <select class="form-select" aria-label="Default select example">
                <option selected>Scegli un tipo di carta!</option>
                <option value="1">One</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
            </select>

            <div class="list-cont p-5 bg-white">
                <!-- qui ci va il componente lista -->
                <AppListCardsVue/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

select {
    width: fit-content;
}

.list-cont {
    height: 900px;
}
</style>
