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

            <div id="text-area">
                <h1>{{ slide.title }}</h1>
                <p class="d-flex"> {{ slide.subtitle }}</p>

                <button class= "text-white px-3 py-3 bg-black d-flex gap-1">
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
    width: 30px;
    height: 30px;
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
        top:50%;
        left:15%;
        color: white;

        button {
            position: relative;
            left: 0;
            border: 0;
        }
}



</style>