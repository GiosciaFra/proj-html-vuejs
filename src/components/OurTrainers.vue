<script>
export default {
    name: 'OurTrainers',

    data() {
        return {
            trainers: [
                {
                    image: 'biker1.jpg',
                    name: 'Michael Lee',
                    job: 'Biker',
                },

                {
                    image: 'biker4.jpg',
                    name: 'Robert Lee',
                    job: 'Biker',
                },

                {
                    image: 'biker3.jpg',
                    name: 'John Doe',
                    job: 'Biker',
                },

                {
                    image: 'biker2.jpg',
                    name: 'Emily Brown',
                    job: 'Biker',

                },
            ]
        }
    }
}
</script>

<template>

    <div class="container-train mt-5">

        
        <div class="text-center pb-5 title">
            
            
            <h2><strong>Our Expert Trainers!</strong></h2>
            <p>Learn to ride a bike from the experts.</p>
        </div>
        
        <div class="d-flex px-4 justify-content-center gap-5 pb-5 ">
            
            <div v-for="trainer in trainers" class="card pippo " style="width: 18rem;">
                <img :src="`/img/${trainer.image}`" class="card-img img-fluid position-relative ">
                <div class="card-body bg-black text-white position-absolute text-center  ">
                    <h5 class="card-title"><strong>{{trainer.name}}</strong></h5>
                    <p class="card-text"><strong>{{trainer.job}}</strong></p>
                    
                    <p class="card-social d-flex justify-content-center gap-2">
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-square-instagram"></i>
                        <i class="fa-brands fa-x-twitter"></i>
                    </p>
                    
                    
                </div>
                
            </div>
        </div>
    </div>
        
</template>

<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/variables.scss' as *; 


.container-train {
    background-color: #fbfbfb;

    .pippo {
        border: 10px solid #F5F5F5;
        
        .card-text {
            color: rgb(186, 173, 173);
        }
    }



    .card-body {
        left: 0;
        bottom: -20px;
        width: 269px;
    }
}



</style>