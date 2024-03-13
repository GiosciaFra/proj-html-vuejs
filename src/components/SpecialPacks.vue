<script>
export default {
    name: 'SpecialPacks',

    data() {
        return{

            packs: [
            {
             front: {
            icon: 'handshake.png',
            title: 'Basic',
            subtitle: 'Learn to bike from the professionals',
            list: ['Item 1', 'Item 2', 'Item 3']
          },
             back: {
            title: 'Basic',
            list: ['Back Item 1', 'Back Item 2', 'Back Item 3']
          }
        },

        {
             front: {
            icon: 'helmet.png',
            title: 'Standard',
            subtitle: 'Learn to bike from the professionals',
            list: ['Item 1', 'Item 2', 'Item 3']
          },
             back: {
            title: 'Standard',
            list: ['Back Item 1', 'Back Item 2', 'Back Item 3']
          }
        },

        {
             front: {
            icon: 'racing-helmet.png',
            title: 'Premium',
            subtitle: 'Learn to bike from the professionals',
            list: ['Item 1', 'Item 2', 'Item 3']
          },
             back: {
            title: 'Premium',
            list: ['Back Item 1', 'Back Item 2', 'Back Item 3']
          }
        },
            ]
        }
      }
}
</script>

<template>

<div class="container-title text-center py-4 title">

    <div class="icon-packs">
        <i class="fa-solid fa-award fa-2xl"></i>
        </div>


        <h2><strong>Special Packs</strong></h2>
        <p>Select pricing plan to get more</p>
</div>

<div class="packs-container d-flex justify-content-center ">

    <div v-for="(pack, index) in packs" :key="index" class="pack ">
      <div class="pack-inner">
        <div class="pack-face front d-flex flex-column">
            <img :src="`/img/${pack.front.icon}`" alt="">
          <h3>{{ pack.front.title }}</h3>
          <ul>
            <li v-for="(item, i) in pack.front.list" :key="i">{{ item }}</li>
          </ul>
        </div>
        <div class="pack-face back d-flex flex-column">
          <img :src="`/img/${pack.front.icon}`" alt="">
          <h3>{{ pack.back.title }}</h3>
          <ul>
            <li v-for="(item, i) in pack.back.list" :key="i">{{ item }}</li>
          </ul>
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
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 24px;
      color: red
    }

    .front {
        background: linear-gradient(-15deg, white 60%, black 40%);
        }

    .back {
        background-color: black;
        transform: rotateY(180deg);
    }


    img {
        width: 80px;
        height: 90px;
    }

</style>