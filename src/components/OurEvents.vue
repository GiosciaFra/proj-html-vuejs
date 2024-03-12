<script>
export default {
    name: 'OurEvents',

    data() {
        return {
            events: [
            {   image: 'event1.jpg', 
                name:'Toronto Cycling Event 2023', 
                date: '2022-06-22 H 01:30 - 2023-08-11  H 07:00 ',
                place: 'Toronto',
                type: 'Bicycle Race',
                tagDay: '22',
                tagMonth: 'JUN'

            },

            {   image: 'event2.jpg', 
                name:'Istanbul Cycling Event 2023', 
                date: '2022-06-22 H 01:30 - 2023-08-11  H 07:00 ',
                place: 'Istanbul',
                type: 'Bike Sport',
                tagDay: '30',
                tagMonth: 'JUN'

            },

            {   image: 'event3.jpg', 
                name:'Paris Cycling Event 2023', 
                date: '2022-06-22 H 01:30 - 2023-08-11  H 07:00 ',
                place: 'Paris',
                type: 'Cycling Tour',
                tagDay: '22',
                tagMonth: 'JUN'

            },

            {   image: 'event4.jpg', 
                name:'New Jersey Cycling Event 2023', 
                date: '2022-06-22 H 01:30 - 2023-08-11  H 07:00 ',
                place: 'New Jersey',
                type: 'Bicycle Race',
                tagDay: '25',
                tagMonth: 'JUN'

            },

            {   image: 'event5.jpg', 
                name:'London Cycling Event 2023', 
                date: '2022-06-22 H 01:30  -  2023-08-11 H 07:00 ',
                place: 'London',
                type: 'Bike Sport',
                tagDay: '28',
                tagMonth: 'JUN'

            },

            {   image: 'event6.jpg', 
                name:'Kiev Cycling Event 2023', 
                date: '2022-06-22 H 01:30  -  2023-08-11 H 07:00 ',
                place: 'Kiev',
                type: 'Bicycle Race',
                tagDay: '29',
                tagMonth: 'JUN'

            },


            {   image: 'event7.jpg', 
                name:'Colorado Cycling Event 2023', 
                date: '2022-06-22 H 01:30  -  2023-08-11 H 07:00 ',
                place: 'Colorado',
                type: 'Bike Sport',
                tagDay: '28',
                tagMonth: 'JUN'

            },


            {   image: 'event8.jpg', 
                name:'Amsterdam Cycling Event 2023', 
                date: '2022-06-22 H 01:30  -  2023-08-11 H 07:00 ',
                place: 'Amsterdam',
                type: 'Bicycle Race',
                tagDay: '28',
                tagMonth: 'JUN'

            },


            {   image: 'event9.jpg', 
                name:'Toronto Cycling Event 2023', 
                date: '2022-06-22 H 01:30  -  2023-08-11 H 07:00 ',
                place: 'Toronto',
                type: 'Bicycle Race',
                tagDay: '22',
                tagMonth: 'JUN'

            },


            {   image: 'event10.jpg', 
                name:'Paris Cycling Event 2023', 
                date: '2022-06-22 H 01:30  -  2023-08-11 H 07:00 ',
                place: 'Paris',
                type: 'Bicycle Race',
                tagDay: '26',
                tagMonth: 'JUN'

            },


        ],

    }
}
}

</script>

<template>
    
    <div class="container text-center pb-5 title">
        

        <h3>Don't Miss Our Events!</h3>
        <p>Get the amazing cycling experience.</p>
</div>
<div class="container gap-4 pb-3 d-flex flex-wrap">

        <div v-for="event in events" class="card position-relative ">
            <img :src="`/img/${event.image}`">
            <div class="card-body d-flex flex-column gap-1">
                <h5 class="card-title"><strong>{{event.name}}</strong></h5>
                <p class="card-text"><i class="fa-regular fa-clock"></i> {{ event.date }}</p>
                <p class="card-text"><i class="fa-solid fa-location-dot"></i> {{ event.place }}</p>
                <p class="type rounded rounded-2 w-25 text-center p-1 ">{{ event.type }}</p>

                <div class="tag shadow-lg position-absolute text-center bg-white  rounded rounded-2">

                    <p class="day">{{ event.tagDay }}</p>
                    <p class="month">{{ event.tagMonth }}</p>


                </div>



            </div>
        </div>
        
    </div>



</template>

<style lang="scss">

@use '../styles/general.scss' as *;
@use '../styles/variables.scss' as *; 

.card {
    max-width: 440px;

    .card-text {
        color: rgb(106, 106, 106);

    }

    .tag {
        top: 10px;
        left: 10px;
        height: 60px;
        width: 60px;
        
        .day {
            font-size:$fontSizeBig;
            font-weight:600;
            
        }

        .month {
            
            font-size: $fontSizeSmall;
        }
        
    }

    .type {
        background-color: #f5f5f5;
        color: rgb(106, 106, 106);
        font-weight: 400;
    }
}

</style>