<script>
export default {
    name: 'ResentNewArticles',

    data() {
        return {
            articles: [
                {
                    image: 'news-bike3.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'Road bike or mountain bike?',
                    text: 'Compared to similar road bikes with a solid frame structure.[...]'
                    
                },

                {
                    image: 'news-bike4.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'What is mountain biking called?',
                    text: 'Mountain bike is one of the most popular outdoor sports.[...]'
                    
                },

                {
                    image: 'news-bike5.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'How much should you cycle a day?',
                    text: 'In order to get the right benefit from the exercise.[...]'
                    
                },

                {
                    image: 'news-bike6.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'How long does it take 5 km by bike?',
                    text: 'It takes 5 km and 10 minutes, sir. But at [...]'
                    
                },
            ]
        }
    },
}
</script>

<template>
    <div class="container text-center pb-5 title ">
        
        <h2><strong>Resent New & Articles</strong></h2>
        <p> Important information about bike</p>

    </div>
<div class="container d-flex justify-content-center  gap-5 ">


    <div v-for="article in articles" class="card shadow border-0 ">
        
        <img :src="`/img/${article.image}`" class=" mx-4 mt-4 ">
        <p class="card-date text-center">{{ article.date }}</p>

        <div class="card-body d-flex flex-column align-items-center">

            <h5 class="card-title justify-content-center"><strong>{{article.title}}</strong></h5>
            <p class="card-text">{{ article.text }}</p>
            <button class="bg-black text-white border-0 px-5 py-3 rounded-1  py-4 "><strong>More</strong></button>
        </div>
    </div>
</div>
</template>

<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/variables.scss' as *; 

.card-title {
    font-size: $fontSizeBig;
}

.card-date {
    margin: 0;
    font-weight: 500;
}




</style>