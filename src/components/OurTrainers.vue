<script>
export default {
    name: 'OurTrainers',

    data() {
        return {
            trainers: [
                {
                    image: 'biker1.jpg',
                    name: 'Michael Lee',
                    
                    social: [
                        '<i class="fa-brands fa-facebook-f"></i>', 
                        '<i class="fa-brands fa-square-instagram"></i>',
                        '<i class="fa-brands fa-x-twitter"></i>'

                    ]
                }
            ]
        }
    }
}
</script>

<template>

<div class="container text-center pb-5 title">
        

        <h3>Our Expert Trainers!</h3>
        <p>Learn to ride a bike from the experts.</p>
</div>

<div class="container">

    <div v-for="trainer in trainers" class="card" style="width: 18rem;">
        <img :src="`/img/${trainer.image}`" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{trainer.name}}</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item">An item</li>
            <li class="list-group-item">A second item</li>
            <li class="list-group-item">A third item</li>
        </ul>
        <div class="card-body">
            <a href="#" class="card-link">Card link</a>
            <a href="#" class="card-link">Another link</a>
        </div>
  </div>
</div>

</template>

<style lang="scss">
</style>