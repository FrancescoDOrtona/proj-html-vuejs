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
        <div class="sidebar__imgs">
            <div class="imgs__recipes">
                <img class="recipes__img" src="/ad-bg.jpg" alt="">
                <p class="recipes__text">View our <br> latest <br> recipes</p>
            </div>
            <div class="imgs__guide">
                <img src="/singapore-featured-image-400x263.jpg" alt="">
                <button class="guide__button"><font-awesome-icon icon="fa-solid fa-earth-americas" /> view all city guides</button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

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
</style>