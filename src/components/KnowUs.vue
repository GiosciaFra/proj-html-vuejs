<script>
export default {
    name: 'KnowUs',
}
</script>

<template>

    <div class="container d-flex justify-content-center ">

        <div class="row pt-5 ">

            <div class="know-left col d-flex justify-content-center  ">
                
                <img src="/public/img/bike-player.png" alt="">
            </div>

            <div class="know-right col d-flex justify-content-center align-items-center ms-3 ">
                    <div class="content">

                        <div class="text">

                            <h2 class="fw-bold">Do you wanto to be a professional cyclist?</h2>
                            
                            <p>We offer 6 courses of varying difficulty and beautiful scenary that cyclist of all levels can enjoy.
                                You wil learn cycling from professionals with our competent and experienced staff.
                                You will have a lot of fun with our amazing space.
                            </p>
                        </div>

                        <img src="/public/img/divider.jpg" alt="">

                        <div class="pro d-flex pt-4 gap-2  ">
                            <img src="/public/img/racing-helmet.png" alt="">
                            
                            <div class="team d-flex flex-wrap ps-3 flex-column pt-2">
                                
                                <h3 class="fw-bold" >Professional Team</h3>
                                <p>We make you professional by adding yuor sincerity as well as professionalism.</p>
                            </div>
                            
                        </div>
                        
                        <div class="pro d-flex pt-4 gap-2">
                            <img src="/public/img/helmet.png" alt="">

                            <div class="train d-flex flex-wrap ps-3 flex-column pt-2 ">
                                <h3 class="fw-bold">Professional Trainings</h3>
                                <p>We always ride with the best equipment, respecting nature and fun.</p>
                            </div>
                        </div>

                        <button class="mt-4 bg-black text-white px-3 py-3">
                            Get to know us
                            <i class="fa-solid fa-arrow-right ps-2 "></i>
                        </button>
                    </div>

 
            </div>

        </div>


    </div>

</template>

<style lang="scss">

@use '../styles/general.scss' as *;
@use '../styles/variables.scss' as *; 


.know-left {
    background-image: url(/public/img/bike-circle.png);
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: center;
    img {
        height: 650px;
        // margin-right: 180px;
        
    }
    // width: 1000px;

}


.know-right {
    max-width: 400px;
    padding-right: 40px;
}
h2 {
    font-size: $fontSizeBig;
}

p {
    font-size: $fontSizeSmall;

}
    .pro {
        img {
            height: 60px;
            width: 60px;
        }

        h3 {
            font-size: $fontSizeMiddle;
        }

         p {
            font-size: $fontSizeSmall;
           }
    }


</style>