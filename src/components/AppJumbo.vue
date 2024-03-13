<script>
export default {
    name: 'AppJumbo',

    data() {
        return {
            slides: [
                { image: 'slider-bike-4.jpg', title: 'Professional Cycling Club', subtitle: 'Learn Cycling from the pros.' },
                { image: 'slider-bike-9.jpg', title: 'Professional Cycling Club', subtitle: 'Learn Cycling from the pros.' },
                { image: 'slider-bike-12.jpg', title: 'Professional Cycling Club', subtitle: 'Learn Cycling from the pros.' },
            ],
        activeSlideIndex: 0,
    };
},

    methods: {
                prevSlide() {
                    this.activeSlideIndex--;
                    if (this.activeSlideIndex < 0) {
                        this.activeSlideIndex = this.slides.length - 1;
                    }
                },

                nextSlide() {
                this.activeSlideIndex++;
                    if (this.activeSlideIndex > this.slides.length - 1) {
                        this.activeSlideIndex = 0;
                    }
                },
            }
        }
</script>

<template>

<div class="slider">
    <div class="slide-container">
        <div v-for="(slide, index) in slides" :key="index" v-show ="index == activeSlideIndex" class=" position-relative ">
            <img :src="`/img/${slide.image}`" alt="Slide" class="img-fluid w-100 object-fit-cover" />

            <div id="text-area" class="d-flex flex-column text-start ">
                <h1 class="ps-5"><strong>{{ slide.title }}</strong></h1>
                
                <p class="ps-5"> <strong>{{ slide.subtitle }}</strong></p>


    <button class= "text-white px-3 py-3 bg-black d-flex gap-1 ms-5 w-50 ali ">
        Learn More
        <i class="fa-solid fa-arrow-right d-flex align-items-center px-1 mt-1"></i>
        
    </button>
            </div>

            <button @click="prevSlide()" class="prev"><i class="fa-solid fa-chevron-left"></i></button>
            <button @click="nextSlide()" class="next"><i class="fa-solid fa-chevron-right"></i></button>
        </div>

    </div>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/variables.scss' as *; 

.slider {
  text-align: center;
  
  .slide-container {
      overflow: hidden;
      
       img {
        height: 600px;
       }
    }
}

.prev, .next {
    width: 50px;
    height: 50px;
    border: none;
    margin: 10px 0;
    background: #231f1f;
    
    position: absolute;
    top: 50%;
    z-index: 9;

    i {
        bottom:2px;
        position: relative;
        color: white;
        font-size: 10px;
    }

    
}

.prev {
    left: 2%;
}
.next {
right: 2%;
}


#text-area {
        position: absolute;
        top:40%;
        left:10%;
        color: white;
        width: 300px;

        p {
            font-size: $fontSizeSmall;
        }

        button {
            position: relative;
            left: 0;
            border: 0;
        }
}



</style>