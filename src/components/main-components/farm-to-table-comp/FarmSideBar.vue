<script>
    export default {
        data() {
            return {
                
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
</style>