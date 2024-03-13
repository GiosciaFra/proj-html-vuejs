<script>

export default {
    name: 'AppFooter',

    props: {
        trainings: {
            type: Array,
            required: true,
        },
        quickLinks: {
            type: Array,
            required: true,
        },
  },
}
</script>

<template>


  <div class=" bg-black text-white mt-5 pt-5 ">
    <div class="d-flex justify-content-around ">
      

        <div class="footer-left">
            <img src="/public/img/logo-footer-gobike.png" alt="Gobike" >

            <div class=" d-flex  align-items-baseline gap-2 pt-4">
                <i class="fa-solid fa-location-dot"></i> <p >New Jersey, USA</p>
            </div>
                <div class="d-flex align-items-baseline gap-2">

                    <i class="fa-solid fa-phone-volume"></i> <p>+1 (234) 567 89 10</p>
                </div>
            <div class="d-flex align-items-baseline gap-2">
                <i class="fa-regular fa-envelope"></i> <p>example@example.com</p>
            </div>
        </div>
      

        <div class="footer-middle d-flex flex-column ">
          <div class="footer-newsletter">
            <h3>Join our newsletter</h3>
            <p>Subscribe to recieve useful information.</p>
            <form action="#">
              <input type="email" placeholder="Il tuo indirizzo email" name="email" class="w-100 p-4">
              <button class="d-flex w-100 p-4 d-flex align-items-center gap-3 bg-white" type="submit">Subscribe<i class="fa-solid fa-arrow-right"></i></button>
            </form>
          </div>
        </div>

        <div class="footer-right  ">
          <div class="footer-links d-flex gap-5 ">
            <div id="trainings">
                <h3 >Trainings</h3>
                <ul class=" d-flex flex-column gap-2 list-unstyled ">
                    <li v-for="train in trainings" :key="link">{{ train.title }}</li>
                </ul>

            </div>

            <div id="quick-links">
                <h3>Quick Links</h3>
                <ul class=" d-flex flex-column gap-2 list-unstyled">
                <li v-for="link in quickLinks" :key="link">{{ link.title }}</li>
                </ul>
            </div>

        </div>
    </div>

    </div>
      
        <div class="footer-bottom text-center py-5 ">
            <p>&copy; 2022 Gobike - Tutti i diritti riservati.</p>
        </div>
</div>



</template>

<style lang="scss" scoped>

img {
    width: 180px;
    height: 80px;
}

// ul {
//     list-style-type:
// }
</style>