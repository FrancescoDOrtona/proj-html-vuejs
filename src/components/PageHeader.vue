<script>

</script>

<template>
    <div class="header">
        <div class="container">
            <div class="header__top-bar">
                <div class="header__links">
                    <a href="#">Download app <span class="badge">IOS</span></a>
                    <a href="#">Advertise with us</a>
                </div>
                <div class="header__socials">
                    <a href="#"><font-awesome-icon icon="fa-brands fa-facebook" /></a>
                    <a href="#"><font-awesome-icon icon="fa-brands fa-instagram" /></a>
                    <a href="#"><font-awesome-icon icon="fa-brands fa-twitter" /></a>
                    <a href="#"><font-awesome-icon icon="fa-brands fa-youtube" /></a>                   
                </div>
            </div>
            <div class="header__logo">
                <img src="/avada-food-logo.png" alt="">
            </div>
        </div>        
    </div>
    
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.header{
    margin: 15px 0px;
}

.header__links{
    font-size: $font-size-sm;
    display: flex;
    gap: 20px;
}
.header__top-bar{
    display: flex;
    justify-content: space-between;
}

.header__socials{
    display: flex;
    gap: 20px;
    font-size: $font-size-sm;
}

.badge{
    background-color: orange;
    padding: 2px 4px;
    border-radius: 4px;
}

.header__logo{
    display: flex;
    justify-content: center;
    margin: 20px 0px;
}

.header__logo img{
    width: 100px;
}
    
</style>