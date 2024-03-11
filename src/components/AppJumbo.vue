<script>
export default {
    name: 'AppJumbo',

    data() {
        return {
            slides: [
            { image: 'slider-bike-4.jpg', text: 'Testo per immagine 1' },
            { image: 'slider-bike-9.jpg', text: 'Testo per immagine 2' },
            { image: 'slider-bike-12.jpg', text: 'Testo per immagine 3' },
            // Aggiungi più oggetti slide con immagini e testi
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
            <!-- <p>{{ slide.text }}</p> -->
            <button @click="prevSlide()" class="prev"></button>
            <button @click="nextSlide()" class="next"></button>
        </div>

    </div>
</div>
</template>

<style lang="scss">
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
    width: 20px;
    height: 20px;
    margin: 10px 0;
    background: #231f1f;
    position: absolute;
    top: 50%;
    z-index: 9;


    
}

.prev {
    left: 2%;
}
.next {
right: 2%;
}

.prev::after {
    content: '';
    width: 10px;
    height: 10px;
    border-left: 1px solid rgb(255, 255, 255);
    border-top: 1px solid rgb(255, 255, 255);
    display: block;
    position: absolute;
    top: 37%;
    left: 50%;
    transform: translate(-50%) rotate(-45deg);
}

.next::before {
    content: '';
    width: 10px;
    height: 10px;
    border-top: 1px solid rgb(255, 255, 255);
    border-left: 1px solid rgb(255, 255, 255);
    display: block;
    position: absolute;
    bottom: 35%;
    left: 50%;
    transform: translate(-50%) rotate(135deg);
}
</style>