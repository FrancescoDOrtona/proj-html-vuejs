<script>
export default{
    data() {
        return {
            foodCards: [
                {
                    imgSrc: '/single-post-img3-400x263.jpg',
                    title: 'Food Corner: Top Japanese Restaurants for Sushi ',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-roundup-400x263.jpg',
                    title: 'Roundup: My New Favourite Recipes For Healty Living',
                    text: 'By Admin | March 25th 2019'
                },
                {
                    imgSrc: '/fi-toasts-400x263.jpg',
                    title: 'Why this Toast With Tea are My New Favorite',
                    text: 'By Admin | March 25th 2019'
                }
            ]
        }
    },
}
</script>

<template>
    <div class="hero">
        <img class="hero__img" src="\single-post-img3-1200x790.jpg" alt="">
        <div class="container-md">
            <div class="hero__card">
                <div class="hero__text">
                    <p>Food Corner: Top Japanese Restaurants for Sushi</p>
                    <p class="hero__text-date">March 25th, 2019</p>
                    <p class="hero__badge">today's pick</p>
                </div>                
            </div>
        </div>
        <div class="container">
            <div class="hero__journal">
                <h3 class="hero__journal-title">Foodie Journal</h3>
                <div class="hero__journal-content">
                    <div class="content__card" v-for="(foodCard, index) in foodCards">
                        <div class="img-position">
                            <img :src="foodCard.imgSrc" alt="">
                            <div class="img-hover">
                                <font-awesome-icon class="circle" icon="fa-solid fa-link" />
                                <p>{{ foodCard.title }}</p>
                            </div>
                        </div>
                        
                        <h4>{{ foodCard.title }}</h4>
                        <small>{{ foodCard.text }}</small>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


.hero{
    position: relative;
    margin-bottom: 140px;
}
.hero__img{
    max-height: 450px;
    object-fit:cover;
    width: 100%;
    position: absolute;
    z-index: -1;
}

.hero__card{
    padding: 110px 0px;
    
}
.hero__text{
    font-size: 30px;
    text-align: center;
    background-color: white;
    border-radius: 15px;
    padding: 30px 0px;
    position: relative;
}

.hero__text-date{
    font-size: $font-size-md;
    color: $grey;
    padding-top: 15px;
}

.hero__badge{
    background-color: $orange;
    padding: 5px 10px;
    font-size: $font-size-sm;
    font-weight: bold;
    color: white;
    text-transform: uppercase;
    border-radius: 10px;
    position: absolute;
    top: 0;
    left: 50%;
    transform: translate(-50%, -50%);
}

.hero__journal{
    background-color: white;
    padding: 20px;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2); 
    box-shadow: 0px 0px 12px 1px rgba(0,0,0,0.2);
}

.hero__journal-title{
    text-align: center;
    margin-bottom: 20px;
    text-transform: uppercase;
}

.hero__journal-content{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 30px;
    text-align: center;
}

.content__card{
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.content__card h4{
    padding: 0px 20px;
}

.content__card small{
    color: $grey;
    font-size: $font-size-sm;
}

</style>