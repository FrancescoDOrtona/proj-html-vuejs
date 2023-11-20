<script>
export default{
    data() {
        return {
            card: {
                img: '/Yogurt-Nan-600x395.jpg',
                title: 'Lunch Favourite with Salad, Naan And Beans',
                subTitle: 'Bakery, Featured, Healty, Latest Recipes, Staff Picks',
                text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus velit similique ducimus ex officiis repellendus deserunt, voluptatem earum. Iure a quaerat aspernatur esse molestias non quam doloremque neque voluptate numquam? Repellendus repudiandae pariatur ut quod assumenda ullam tenetur laborum obcaecati.',
                button: 'Learn More'
            },
            images:['/Mixed-fruits-460x295.jpg',
                    '/r-rachel-park-366508-unsplash-min-460x295.jpg',
                    '/r-michelle-tsang-500721-unsplash-min-460x295.jpg',
                    '/quick-summer-drink-460x295.jpg',
                    '/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg',
                    '/perfect-cosmopolitan-460x295.jpg',
                    '/fi2x-6-460x295.jpg',
                    'r-brooke-lark-96398-unsplash-min-460x295.jpg'
                ]
        }
    },
}
</script>

<template>
    <div class="pop-recipes">
        <div class="container-md pop-recipes__title">
            <h3>Popular Recipes</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Animi quis libero saepe quae at dolorem vero voluptatum non temporibus cumque!</p>
        </div>
        <div class="container">
            <div class="grid">
                <div class="card">
                    <div class="img-position">                        
                            <img :src="card.img" alt="">                                            
                        <div class="img-hover">
                            <font-awesome-icon class="circle" icon="fa-solid fa-link" />
                            <p>{{ card.title }}</p>
                        </div>
                    </div>
                    <div class="card__content">
                        <div class="card__title">
                            <h4>{{ card.title }}</h4>
                            <small>{{ card.subTitle }}</small>
                        </div>
                        <div class="card__text">
                            <p>{{ card.text }}</p>
                            <button class="btn">{{ card.button }}</button>
                        </div>
                    </div>
                </div>
                <div class="img-collection">
                    <div class="grid">
                        <img v-for="(image,index) in images" :src="image" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.pop-recipes{
    margin-bottom: 140px;
}

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
    padding-bottom: 35px;
}

.card__text{
    padding-top: 35px;
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