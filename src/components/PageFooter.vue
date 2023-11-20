<script>
export default{
    data() {
        return {
            carouselImg: [
                {
                    imgSrc:'/Yogurt-Nan-600x395.jpg',
                    description: 'Lunch Favourite with Salad, Naan And Beans' 
                },
                {
                    imgSrc:'/Mixed-fruits-600x395.jpg',
                    description: 'Fruit Platter with Banana, Orange and Mango' 
                },
                {
                    imgSrc:'/r-rachel-park-366508-unsplash-min-600x395.jpg',
                    description: 'Breakfast Table with Waffer, Eggs and Fruits' 
                },
                {
                    imgSrc:'/r-michelle-tsang-500721-unsplash-min-600x395.jpg',
                    description: 'Cups with Cioccolate, Cream & Pistachio Ice Cream ' 
                },
        ],

        pageSections: [
            'Recipes', 'Places', 'Blog', 'About', 'Contact'
        ]
        }
    },
}
</script>

<template>
    <div class="footer">
        <div class="footer__bg">
            <div class="container">
                <div class="footer__subscribe">            
                    <div class="subscribe__title">
                        <h2>Subscribe <span class="color-orange">&</span> Receive A Free eBook</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vero, perferendis quos nesciunt sint numquam sit!</p>
                    </div>            
                    <div class="subscribe__email">
                        <input class="subscribe__input" type="email" placeholder="Insert your email..">
                        <button class="subscribe__btn">Subscribe</button>
                    </div>
                    <p>Lorem ipsum dolor sit amet consectetur.</p>
                </div>     
            </div>
        </div>
        <div class="grid">
           <div class="img-position" v-for="(img,index) in carouselImg">
            <img :src="img.imgSrc" alt="">
            <div class="img-hover">
                <font-awesome-icon class="circle" icon="fa-solid fa-link" />
                <p>{{ img.description }}</p>
            </div>
           </div>
        </div>
        <div class="footer-summary">
            <div class="container">
                <div class="grid">
                    <div class="border-dotted summary__logo">
                        <img src="/avada-food-logo-mob-2x-200x87.png" alt="">
                        <div class="logo__icons">
                            <a href="#"><font-awesome-icon icon="fa-brands fa-facebook" /></a>
                            <a href="#"><font-awesome-icon icon="fa-brands fa-instagram" /></a>
                            <a href="#"><font-awesome-icon icon="fa-brands fa-twitter" /></a>
                            <a href="#"><font-awesome-icon icon="fa-brands fa-youtube" /></a>  
                        </div>
                    </div>
                    <div class="border-dotted">
                        <ul class="footer__sections">
                            <li v-for="(section,index) in pageSections">
                                <a href="#">{{ section }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="border-dotted footer__contacts">
                        <h4 class="color-orange">Contact</h4>
                        <div class="contacts">
                            <font-awesome-icon icon="fa-solid fa-location-dot" />
                            <p>775 New York Ave, Broohlyn, Kings, New York 11203</p>
                        </div>
                        <div class="contacts">
                            <font-awesome-icon icon="fa-solid fa-phone-flip" />
                            <p>+0100-505-0000</p>
                        </div>
                        <div class="contacts">
                            <font-awesome-icon icon="fa-solid fa-envelope" />
                            <p>info@your-domain.com</p>
                        </div>
                    </div>
                    <div class="footer__app">
                        <h4 class="color-orange">Get our App</h4>
                        <div class="app__imgs">
                            <img src="/download-android-200x66.png" alt="">
                            <img src="/download-app-store-200x66.png" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer__copyright">
            <div class="container">
                <div class="copyright">
                    <font-awesome-icon icon="fa-regular fa-copyright" />
                    <span>Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Right Reserved | Powered by WordPress</span>
                </div>                
            </div>
        </div>             
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.footer__bg{
    background-image: url('/subscribe-sec-bg.png');
    background-color: white;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 430px;
    display: flex;
    align-items: center;
}
.footer__subscribe{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;
}

.subscribe__title{
    text-align: center;
}

.subscribe__title h2{
    margin-bottom: 20px;
    font-style: italic;
}

.subscribe__email{
    width: 100%;
    padding: 0px 50px;
    display: flex;
    gap: 20px;
}

.subscribe__btn{
    padding: 10px 50px;
    background-color: $orange;
    border-radius: 3px;
    color: white;
    text-transform: uppercase;
}

.subscribe__input{
    width: 100%;
    border: 1px solid lightgray;
    border-radius: 5px;
    padding: 0px 10px;
}

.grid{
    display: grid;
    grid-template-columns: repeat(4,1fr);
}

.color-orange{
    color: $orange;
}

.footer-summary{
    padding: 80px 0px;
    background-color: white;
}

.summary__logo{
    display: flex;
    flex-direction: column;
    gap: 30px;
    padding: 0px 30px;
}

.summary__logo img{
    width: 70%;
}

.logo__icons{
    display: flex;
    gap: 10px;
    color: gray;
}

.footer__sections{
    display: flex;
    flex-direction: column;
    gap: 20px;
    font-weight: bold;
    font-size: $font-size-sm;
    padding: 0px 30px;
}

.contacts{
    display: flex;
    align-items: baseline;
    gap: 10px;
}

.footer__contacts{
    display: flex;
    flex-direction: column;
    gap: 20px;
    font-size: $font-size-sm;
    padding: 0px 30px;
}

.footer__contacts h4{
    text-transform: uppercase;
    font-size: $font-size-md;
}
.app__imgs{
    display: flex;
    flex-direction: column;
    gap: 15px;
    width: 70%;
}

.footer__app{
    padding: 0px 30px;
}

.footer__app h4{
    text-transform: uppercase;
    margin-bottom: 20px;
    font-size: $font-size-md;
}

.border-dotted{
    border-right: 1px dotted gray;
}

.footer__copyright{
    padding: 30px 0px;
    font-size: $font-size-sm;
    font-weight: bold;
}

.copyright{
    display: flex;
    gap: 5px;
    justify-content: center;
    align-items: center;
}
</style>