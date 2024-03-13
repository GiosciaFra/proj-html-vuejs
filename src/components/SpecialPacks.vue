<script>
export default {
    name: 'SpecialPacks',

    data() {
        return{

            packs: [
            {
             front: {
            icon: 'handshake-white.png',
            title: 'Basic',
            subtitle: 'Learn to bike from the professionals',
            list: ['✓ Phone Mountaineer bike training', 
                    '✓ Remote Excellent bike service', 
                    '✓ Onsite Safe cycling training', 
                    '✗ Saafety helmet on bike', 
                    '✗ Free bikes for children']
          },
             back: {
            title: 'Basic',
            price: '$1000',
            button: 'Send Request!'
          }
        },

        {
             front: {
            icon: 'helmet-white.png',
            title: 'Standard',
            subtitle: 'Learn to bike from the professionals',
            list: ['✓ Phone Mountaineer bike training', 
                    '✓ Remote Excellent bike service', 
                    '✓ Onsite Safe cycling training', 
                    '✗ Saafety helmet on bike', 
                    '✗ Free bikes for children']
          },
             back: {
            title: 'Standard',
            price: '$3000',
            button: 'Send Request!'
          }
        },

        {
             front: {
            icon: 'racing-helmet-white.png',
            title: 'Premium',
            subtitle: 'Learn to bike from the professionals',
            list: ['✓ Phone Mountaineer bike training', 
                    '✓ Remote Excellent bike service', 
                    '✓ Onsite Safe cycling training', 
                    '✗ Saafety helmet on bike', 
                    '✗ Free bikes for children']
          },
             back: {
            title: 'Premium',
            price: '$5000',
            button: 'Send Request!'
          }
        },
            ]
        }
      }
}
</script>

<template>

<div class="container-title text-center justify-content-center align-items-center  py-4 title">


    <div class=" d-flex justify-content-center align-items-center mb-3">
        <div class="icon-aw d-flex justify-content-center align-items-center">
            <img src="/public/img/medal.png" alt="">
        </div>
    </div>



        <h2><strong>Special Packs</strong></h2>
        <p>Select pricing plan to get more</p>
</div>

<div class="packs-container d-flex justify-content-center ">

    <div v-for="(pack, index) in packs" :key="index" class="pack shadow-lg  ">
      <div class="pack-inner">
        
            <div class="pack-face front d-flex flex-column align-items-center gap-3 text-white ">
                <img :src="`/img/${pack.front.icon}`" alt="" class="mt-4" >
                <h4><strong>{{ pack.front.title }}</strong></h4>
                <p class=" fs-6 my_padding "> {{ pack.front.subtitle }}</p>


                <ul class="list-unstyled text-black fs-6 d-flex flex-column  gap-4 text-center   ">
                    <li class=" border-bottom " v-for="(item, i) in pack.front.list" :key="i">{{ item }}</li>
                </ul>
            </div>


            <div class="pack-face back d-flex flex-column justify-content-center text-white align-items-center ">
                <h3><strong>{{ pack.back.title }}</strong></h3>
                <p class="pb-5 fs-2"><strong>{{ pack.back.price }}</strong></p>

                <button class="mt-5 border bg-black text-white px-5 py-4"><strong>{{ pack.back.button }}</strong></button>
            </div>
      </div>
    </div>
</div>    

</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/variables.scss' as *; 

.packs-container, .container-title{

    background-color: #fbfbfb;

}
.pack {
      width: 430px;
      height: 625px;
      perspective: 1000px;
      margin: 20px;
      cursor: pointer;
    }

    .pack-inner {
      width: 100%;
      height: 100%;
      transform-style: preserve-3d;
      transition: transform 0.5s;
    }

    .pack:hover .pack-inner {
      transform: rotateY(180deg);
    }

    .pack-face {
      width: 100%;
      height: 100%;
      position: absolute;
      backface-visibility: hidden;
    }

    .front {
        background: linear-gradient(-5deg, white 60%, rgb(0, 0, 0) 40%);
        }

    .back {
        background-color: black;
        transform: rotateY(180deg);
    }


    img {
        width: 85px;
        height: 85px;
    }

    .my_padding {
        padding-bottom: 100px;
    }

    button {
        font-size: 15px;
    }


    .icon-aw {
        width: 80px;
        height: 80px;
        background-color: black;
    }
</style>