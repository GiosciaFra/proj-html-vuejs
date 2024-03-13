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
          <p>Gobike</p>
          <p>De Chib</p>
          <p>New Jersey, USA</p>
          <p>+1 (234) 567 89 10</p>
        </div>
      

        <div class="footer-middle">
          <div class="footer-newsletter">
            <h3>Iscriviti alla nostra newsletter</h3>
            <p>Iscriviti per ricevere informazioni utili.</p>
            <form action="#">
              <input type="email" placeholder="Il tuo indirizzo email" name="email">
              <button type="submit">Iscriviti</button>
            </form>
          </div>
        </div>

        <div class="footer-right  ">
          <div class="footer-links d-flex gap-4 ">
            <div id="trainings">
                <h3 >Trainings</h3>
                <ul>
                    <li v-for="train in trainings" :key="link">{{ train.title }}</li>
                </ul>

            </div>

            <div id="quick-links">
                <h3>Quick Links</h3>
                <ul>
                <li v-for="link in quickLinks" :key="link">{{ link.title }}</li>
                </ul>
            </div>

        </div>
    </div>

    </div>
      
        <div class="footer-bottom text-center ">
            <p>&copy; 2022 Gobike - Tutti i diritti riservati.</p>
        </div>
</div>



</template>

<style lang="scss">
</style>