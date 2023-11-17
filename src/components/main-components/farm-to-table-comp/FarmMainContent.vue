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
    }
}
}
</script>

<template>
    <div>
        <div class="card">
            <img :src="card.img" alt="">
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
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.card{
    background-color: white;

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
    
</style>