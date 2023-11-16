<script>
import MainHero from './main-components/MainHero.vue'
import PopularRecipes from './main-components/PopularRecipes.vue'

export default {
    components: {
        MainHero,
        PopularRecipes,
    }
}
</script>

<template>
    <MainHero/>
    <PopularRecipes/>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


</style>