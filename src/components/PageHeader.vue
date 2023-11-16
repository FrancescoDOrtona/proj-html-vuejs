<script>
export default{
    data() {
        return {
            navbar: ['Home', 'Recipes', 'Blog', 'About', 'Contact']
        }
    },
}
</script>

<template>
    <div class="header">
        <div class="container">
            <div class="header__top-bar">
                <div class="header__links">
                    <div>
                        <a href="#">Download app</a>
                        <span class="badge">IOS</span>
                    </div>
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
        <div class="container-md">
            <nav class="navbar">
                <ul class="navbar__items">
                    <li v-for="(item,index) in navbar">{{ item }}</li>
                    <li><font-awesome-icon icon="fa-solid fa-magnifying-glass"/></li>
                </ul>
            </nav>           
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

.header__socials a{
    color: lightgrey;
}

.badge{
    background-color: $orange;
    padding: 2px 4px;
    border-radius: 4px;
    font-weight: bold;
    margin-left: 7px;
}

.header__logo{
    display: flex;
    justify-content: center;
    margin-top: 20px;
    margin-bottom: 40px;
}

.header__logo img{
    width: 100px;
}

.navbar__items{
    display: flex;
    gap: 10px;
    justify-content: space-between;
}

.navbar__items li{
    border-bottom: 2px solid transparent;
    padding-bottom: 10px;
}
.navbar__items li:hover{
    color: $orange;
    border-color: $orange;
}
    
</style>