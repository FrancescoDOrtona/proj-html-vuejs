<script>
export default {
    data() {
    return {
        card: {
                img: '/single-post-img3-800x527.jpg',
                title: 'Food Corner: Top Japanese Restaurants for Sushi',
                subTitle: 'By Admin | March 25th 2019',
                text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus velit similique ducimus ex officiis repellendus deserunt, voluptatem earum. Iure a quaerat aspernatur esse molestias non quam doloremque neque voluptate numquam? Repellendus repudiandae pariatur ut quod assumenda ullam tenetur laborum obcaecati.',
                link: 'Read More'
            },
            foodCards: [
                {
                    imgSrc: '/fi-roundup-400x263.jpg',
                    title: 'Roundup: My New Favourite Recipes For Healthy Living',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-korean-food-400x263.jpg',
                    title: 'Meal Prep: Korean Bibimbap with Kimchi',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-toasts-400x263.jpg',
                    title: 'Why this Toast With Tea are My New Favorite',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-street-food-400x263.jpg',
                    title: 'Exploring Street Food in Bangkok',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-organic-breakfast-400x263.jpg',
                    title: 'Organic Choices For Healthier Living',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-water-side-rest-400x263.jpg',
                    title: '5 Waterside Restaurants in Instanbul for Special Events',
                    text: 'By Admin | March 25th 2019'
                },
            ]
    }
}
}
</script>

<template>
    <div>
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
                    <div class="card__footer">
                        <a href="#">{{ card.link }} <font-awesome-icon icon="fa-solid fa-chevron-right" size="2xs"/></a>
                        <div class="card__footer-comments">
                            <font-awesome-icon icon="fa-regular fa-comments" />
                            <span>0</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="posts">
            <div class="posts__content" v-for="(foodCard, index) in foodCards">
                <img :src="foodCard.imgSrc" alt="">
                <h4>{{ foodCard.title }}</h4>
                <small>{{ foodCard.text }}</small>
            </div>
        </div>
        <button class="posts__btn">Load More Posts</button>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.card{
    background-color: white;
    margin-bottom: 40px;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2); 
    box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2);
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

.card__footer{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.card__footer-comments{
    display: flex;
    align-items: center;
    gap: 5px;
}

.posts{
    display: grid;
    grid-template-columns: repeat(2,1fr);
    gap: 30px;
    text-align: center;
}

.posts__content{
    display: flex;
    flex-direction: column;
    gap: 15px;
    background-color: white;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2); 
    box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2);
}

.posts__content h4{
    padding: 0px 20px;
}

.posts__content small{
    color: $grey;
    font-size: $font-size-sm;
    padding-bottom: 20px;
}

.posts__btn{
    width: 100%;
    background-color: lightgrey;
    border-radius: 0px;
    margin-top: 40px;
    text-transform: uppercase;
}
    
</style>