<script>
import PageHeader from './components/PageHeader.vue'
import PageMain from './components/PageMain.vue'
import PageFooter from './components/PageFooter.vue'

export default{
    components: {
        PageHeader,
        PageMain,
        PageFooter,
    },
    data() {
        return {
            message: 'test'
        }
    }
}
</script>

<template>
  <PageHeader/>
  <PageMain/>
  <PageFooter/>
</template>

<style lang="scss">
@use '../style/partials/general.scss'

</style>
