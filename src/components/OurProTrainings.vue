<script>

export default {
    name: 'OurProTrainings',

    data() {
        return {
            slides: [
            { image: 'training-box-1.jpg', text:'Riding Lesson' },
            { image: 'training-box-2.jpg', text:'Safe Driving'},
            { image: 'training-box-3.jpg', text:'Mountain bike' },
            { image: 'training-box-4.jpg', text:'Trail Drive' },

        ],

    }
}
}




</script>


<template>
    <div class="container text-center pb-3 title">
        

            <h2><strong>Our Professional Cycling Trainings</strong></h2>
            <p>Learn from the mountain biking expert.</p>
    </div>

    <div class="container d-flex justify-content-center  align-items-center ">
        
            
            <div v-for="slide in slides" class="d-flex gap-2 position-relative ">
                <div class=" contras mx-3 border border-5  border-black  "><img :src="`/img/${slide.image}`" alt="" class="photo"></div>
                <div class="text-slide text-white position-absolute  ">
                    <h4><strong>{{ slide.text }}</strong></h4>

                </div>
            </div>
        
            
            
        </div>
        
        <div class="container d-flex justify-content-center  align-items-center buttons gap-2 ">
            
            <button class=" bg-white "><i class="fa-solid fa-chevron-left"></i></button>
            <button class=" bg-white "><i class="fa-solid fa-chevron-right"></i></button>
        </div>


</template>


<style lang="scss" >

@use '../styles/general.scss' as *;
@use '../styles/variables.scss' as *; 

.title {
    padding-top: 120px;
}

.photo{
filter: brightness(60%);
}

.text-slide{ 
        top:25px;
        left:45px;
}

.buttons {

    padding-top: 70px;

    button{
        width: 60px;
        height: 60px;
    }

}



</style>