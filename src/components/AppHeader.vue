<script>


export default {
    name: 'AppHeader',


    props: {
        links: {
            type: Array,
            required: true,
        }
    }
}



</script>

<template>
    <div class="container">
        <nav class="navbar d-flex justify-content-around align-items-center  ">


                <div id="logo" class="d-flexalign-items-center h-100">

                    <img src="/public/img/logo-gobike.png" alt="Logo" class="logo img-fluid ">
                </div>

         

                <div id="links" class="d-flex align-items-center h-100 ">

                    <ul class="nav-links d-flex list-unstyled gap-2   ">
                        <li v-for="(link, index) in links" :key="index">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
        
                    </ul>
                </div>

                <div id="right-nav" class="d-flex gap-2 h-100 align-items-center pb-3">

                    <div>
                        <i class="fa-solid fa-bars"></i>
                    </div>

                    <button class=" bg-black text-white px-2 py-2">
                        <img class="helmet pe-2 " src="/public/img/helmet.jpg" alt="">
                             Upcoming Events 
                        <i class="fa-solid fa-arrow-right ps-2 "></i>
                    </button>


                </div>

        </nav>
    </div>
</template>

<style lang="scss">
@use '../styles/general.scss' as *;

.navbar {
    height: 92px;
    .logo {
        height: 60px;
        width: 200px;
    }

    a {
        text-decoration: none;
        list-style: none;
        color: black;
    }
    .helmet {
        height: 40px;
    }
}


</style>