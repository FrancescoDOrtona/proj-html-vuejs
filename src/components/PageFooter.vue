<script>

</script>

<template>
    <div class="footer">
        <div class="footer__bg">
            <div class="container">
                <div class="footer__subscribe">            
                    <div class="subscribe__title">
                        <h2>Subscribe & Receive A Free eBook</h2>
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
                      
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.footer__bg{
    background-image: url('/subscribe-sec-bg.png');
    background-color: white;
    background-position: center;
    background-size: cover;
    min-height: 400px;
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
</style>