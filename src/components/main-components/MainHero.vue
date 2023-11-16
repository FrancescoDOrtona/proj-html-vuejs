<script>

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
                <h3>Foodie Journal</h3>
                <div>
                    <img src="/single-post-img3-400x263.jpg" alt="">
                    <h5>Food Corner</h5>
                    <small>by...</small>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


.hero{
    position: relative;
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


</style>