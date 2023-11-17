<script>
import FarmMainContent from './farm-to-table-comp/FarmMainContent.vue'
import FarmSideBar from './farm-to-table-comp/FarmSideBar.vue'

export default{
    components: {
        FarmMainContent,
        FarmSideBar,
    },
    
    data() {
        return {
            
        }
    },
}

</script>

<template>
    <div class="farm">
       <div class="container">
        <div class="farm__title">
            <div class="title__content">
                <h3>Farm to table</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi, corporis nostrum minus laudantium quae quidem.</p>
            </div>
            <div>
                <button class="title__button"> Read our blog <font-awesome-icon class="blog-icon" icon="fa-solid fa-book-open-reader"/></button>
            </div>
        </div>
        <div class="grid">
            <div class="farm__main">
                <FarmMainContent/>
            </div>
            <div class="farm-sidebar">
                <FarmSideBar/>
            </div>
        </div>
       </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.farm__title{
    display: flex;
    justify-content: space-between;
}

.farm__title h3{
    text-transform: uppercase;
}

.farm__title p{
    font-size: $font-size-sm;
    color: $grey;
    padding: 30px 0px;
}

.title__content{
    width: 50%;
}

.title__button{
    background-color: $orange;
    border-radius: 0px;
    color: white;
    font-size: $font-size-sm;
    text-transform: uppercase;
}

.blog-icon{
    margin-left: 5px;
}

.grid{
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 40px;
}
    
</style>