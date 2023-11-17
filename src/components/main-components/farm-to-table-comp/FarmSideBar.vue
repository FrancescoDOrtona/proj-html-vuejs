<script>
    export default {
        data() {
            return {
                treads: [
                    {
                        imgSrc: '/single-post-img3-66x66.jpg',
                        title: 'Food Corner: Top Japanese Restaurants for Sushi',
                        date: 'March 25th,2019',
                    },
                    {
                        imgSrc: '/singapore-featured-image-66x66.jpg',
                        title: 'City Guide: Singapore',
                        date: 'February 27th,2019',
                    },
                    {
                        imgSrc: '/slide1-bg-66x66.jpg',
                        title: '6 Nutritional Tips to Help Burn Body Fat',
                        date: 'February 28th,2019',
                    },
                ]
            }
        },
    }
</script>

<template>
    <div class="sidebar">
        <!-- Latest recipe & City guides images -->
        <div class="sidebar__imgs">
            <div class="imgs__recipes">
                <img class="recipes__img" src="/ad-bg.jpg" alt="">
                <p class="recipes__text">View our <br> latest <br> recipes</p>
            </div>
            <div class="imgs__guide">
                <img class="guide__img" src="/singapore-featured-image-400x263.jpg" alt="">
                <span class="label">City guide: Singapore</span>
                <button class="guide__button"><font-awesome-icon icon="fa-solid fa-earth-americas" /> view all city guides</button>
            </div>
        </div>

        <!-- Search -->
        <div class="sidebar__search">
            <input type="search" name="search" id="sidebar-search" placeholder="Search..">
        </div>

        <!-- Follow us -->
        <div class="follow">
            <h5>Follow Us</h5>
            <div class="follow__socials">
                <a class="socials__icon" href="#"><font-awesome-icon icon="fa-brands fa-facebook" /></a>
                <a class="socials__icon" href="#"><font-awesome-icon icon="fa-brands fa-instagram" /></a>
                <a class="socials__icon" href="#"><font-awesome-icon icon="fa-brands fa-twitter" /></a>
                <a class="socials__icon" href="#"><font-awesome-icon icon="fa-brands fa-youtube" /></a>
                <a class="socials__icon" href="#"><font-awesome-icon icon="fa-brands fa-pinterest" /></a>
            </div>
        </div>

        <!-- Popular & recents treads -->
        <div class="treads">
            <div class="treads__heading">
                <div class="grid">
                    <div class="heading__text bg-color-white">
                        <h5>Popular</h5>
                    </div>
                    <div class="heading__text">
                        <h5>Recent</h5>
                    </div>
                </div>
            </div>
            <div class="cards">
                <div v-for="(tread,index) in treads" class="card">
                    <img class="card__img" :src="tread.imgSrc" alt="">
                    <div>
                        <h4>{{ tread.title }}</h4>
                        <small>{{ tread.date }}</small>
                    </div>
                </div>
            </div>
        </div>
        <div class="tweets">
            <div class="tweets__header">
                <h3>Tweets <span class="header__text">by</span> <span class="header__text color-blue">@Theme_Fusion</span></h3>
                <font-awesome-icon icon="fa-solid fa-circle-info" />
            </div>
            <div class="tweets_content">
                <div class="tweets__logo">
                    <img  src="/3a74ce3d0532b7773b174c45ca3bd05a_normal.png" alt="">
                </div>
                <div>
                    <div class="tweets__header">
                        <h5>ThemeFusion</h5>
                        <font-awesome-icon class="color-light-grey" icon="fa-brands fa-twitter" />
                    </div>
                    <small class="color-blue">@Theme_Fusion</small>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nobis totam, alias ullam atque, quo corrupti, sunt aut vitae provident eius quidem expedita dolor dolore voluptatibus possimus ea nemo corporis reprehenderit.</p>
                    <img class="tweets__img" src="/En2TRxLW4AEiWUN.jpeg" alt="">
                    <div class="tweets__footer">
                        <div class="tweets__icons">
                            <a href=""><font-awesome-icon icon="fa-regular fa-heart" /></a>
                            <a href=""><font-awesome-icon icon="fa-solid fa-arrow-right-from-bracket" /></a>                           
                        </div>
                        <p>21<span class="text-underline">h</span></p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.sidebar__imgs{
    border-bottom: 1px solid lightgray;
}

.imgs__recipes{
    position: relative;
}

img{
    display: block;
}

.recipes__text{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-transform: uppercase;
    text-align: center;
    font-weight: bold;
}

.imgs__guide{
    margin: 30px 0px;
    position: relative;
}

.guide__button{
    background-color: $orange;
    width: 100%;
    text-align: center;
    text-transform: uppercase;
    font-size: $font-size-sm;
    border-radius: 0px;
    color: white;
}


.label{
    position: absolute;
    top: 50%;
    left: 0;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.8);
    color: white;
    font-weight: bold;
    font-size: 14px;
}

.sidebar__search{
    margin: 30px 0px;
}

#sidebar-search{
    width: 100%;
    padding: 10px;
    border: 1px solid lightgray;
    border-radius: 5px;
}

.follow h5{
    color: $orange;
}

.follow__socials{
    margin: 20px 0px;
    display: flex;
    gap: 10px;
    align-items: center;
}

.socials__icon{
    padding: 3px 6px;
    background-color: lightgray;
    border-radius: 3px;
}

.grid{
    display: grid;
    grid-template-columns: repeat(2,1fr);
}

.treads__heading{
    margin: 30px 0px;
}

.heading__text{
    display: flex;
    justify-content: center;
    border: 1px solid lightgray;
    padding: 10px
}

.bg-color-white{
    background-color: white;
}

.card__img{
    border-radius: 50%;
    width: 50px;
    aspect-ratio: 1;
}

.cards{
    display: flex;
    flex-direction: column;
    gap: 35px;
    margin-bottom: 30px;
}
.card{
    display: flex;
    align-items: center;
    gap: 20px;
}

.card h4{
    font-size: 14px;
}

.tweets{
    padding: 20px;
    background-color: white;
    border-radius: 10px;
}

.tweets__header{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.header__text{
    font-size: 12px;
}

.tweets__logo{
    width: 100%;
}
.tweets_content{
    display: flex;
    gap: 15px;
    margin-top: 15px;
}

.tweets__img{
    border-radius: 5px;
    margin-top: 20px;
}

.tweets__footer{
    padding: 20px 0px;
    display: flex;
    justify-content: space-between;
}

.tweets__footer p{
    font-size: $font-size-sm;
}

.text-underline{
    text-decoration: underline;
}

.color-blue{
    color: blue;
}

.color-light-grey{
    color: lightgray;
}

.tweets__icons{
    display: flex;
    gap: 30px;
}
</style>