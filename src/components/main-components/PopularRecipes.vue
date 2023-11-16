<script>

</script>

<template>
    <div>
        <div class="container-md pop-recipes__title">
            <h3>Popular Recipes</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Animi quis libero saepe quae at dolorem vero voluptatum non temporibus cumque!</p>
        </div>
        <div class="container">
            <div class="grid">
                <div class="card">
                    <img src="/Yogurt-Nan-600x395.jpg" alt="">
                    <div class="card__content">
                        <div class="card__title">
                            <h4>Lunch Favourite with Salad, Naan And Beans</h4>
                            <small>Bakery, Featured, Healty, Latest Recipes, Staff Picks</small>
                        </div>
                        <div class="card__text">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus velit similique ducimus ex officiis repellendus deserunt, voluptatem earum. Iure a quaerat aspernatur esse molestias non quam doloremque neque voluptate numquam? Repellendus repudiandae pariatur ut quod assumenda ullam tenetur laborum obcaecati.</p>
                            <button class="btn">Learn More</button>
                        </div>
                    </div>
                </div>
                <div class="img-collection">
                    ciao
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.pop-recipes__title{
    text-align: center;
}

.pop-recipes__title h3{
    text-transform: uppercase;
}

.pop-recipes__title p{
    font-size: $font-size-sm;
    color: $grey;
    padding: 30px 0px;
}

.grid{
    display: grid;
    grid-template-columns: repeat(2,1fr);
    gap: 40px;
}

.card{
    background-color: white;

}

.card__content{
    padding: 30px;
}
.card__title{
    border-bottom: 2px solid lightgray;
    padding-bottom: 20px;
}

.card__text{
    padding-top: 20px;
}

.card__text p{
    margin-bottom: 20px;
}

.btn{
    color: white;
    background-color: $orange;
    border-radius: 0px;
}   
</style>