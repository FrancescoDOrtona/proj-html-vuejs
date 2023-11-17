<script>
import MainHero from './main-components/MainHero.vue'
import PopularRecipes from './main-components/PopularRecipes.vue'
import CulinaryCollection from './main-components/CulinaryCollection.vue';

export default {
    components: {
        MainHero,
        PopularRecipes,
        CulinaryCollection,
    }
}
</script>

<template>
    <MainHero/>
    <PopularRecipes/>
    <CulinaryCollection/>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


</style>