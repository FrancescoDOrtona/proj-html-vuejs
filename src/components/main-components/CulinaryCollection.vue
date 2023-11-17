<script>
export default{
    data() {
        return {
            recipes:[
                {
                    imgSrc: '/drinks-recipes.png',
                    name: 'drinks'
                },
                {
                    imgSrc: '/soups-recipes.png',
                    name: 'soups'
                },
                {
                    imgSrc: '/baking-recipes.png',
                    name: 'bakery'
                },
                {
                    imgSrc: '/dinner-recipes.png',
                    name: 'dinner'
                },
                {
                    imgSrc: '/healthy-recipes.png',
                    name: 'healty'
                },
                {
                    imgSrc: '/staff-picks.png',
                    name: 'staff picks'
                },
                {
                    imgSrc: '/premium-recipes.png',
                    name: 'appetisers'
                },
                {
                    imgSrc: '/quick-easy-recipes.png',
                    name: 'quick & easy'
                },
            ]

        }
    },
}

</script>

<template>
    <div class="collection">
        <div class="container-md collection__title">
            <h3>Culinary Collection</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Animi quis libero saepe quae at dolorem vero voluptatum non temporibus cumque!</p>
        </div>
        <div class="container">
            <div class="grid">
                <div class="collection__card" v-for="(recipe, index) in recipes">
                    <img :src="recipe.imgSrc" alt="">
                    <h4>{{ recipe.name }}</h4>
                </div>               
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.collection{
    margin-bottom: 40px;
}

.collection__title{
    text-align: center;
}

.collection__title h3{
    text-transform: uppercase;
}

.collection__title p{
    font-size: $font-size-sm;
    color: $grey;
    padding: 30px 0px;
}

.grid{
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 20px;
}

.collection__card{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 15px;
    background-color: white;
    padding: 20px;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2); 
    box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2);
}

.collection__card img{
    width: 40%;
}

.collection__card h4{
    text-transform: uppercase;
    font-size: $font-size-sm;
}
</style>