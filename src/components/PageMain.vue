<script>
import MainHero from './main-components/MainHero.vue'
import PopularRecipes from './main-components/PopularRecipes.vue'
import CulinaryCollection from './main-components/CulinaryCollection.vue';
import FarmToTable from './main-components/FarmToTable.vue';

export default {
    components: {
        MainHero,
        PopularRecipes,
        CulinaryCollection,
        FarmToTable,
    }
}
</script>

<template>
    <MainHero/>
    <PopularRecipes/>
    <CulinaryCollection/>
    <FarmToTable/>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


</style>