<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'


export default {
   components: {
    AppHeader,
    AppMain,
    AppFooter
   },

   data() {
    return {
        navLinks: [
        { text: 'Home', url: '#' },
        { text: 'About Us', url: '#' },
        { text: 'Trainings', url: '#' },
        { text: 'Packages', url: '#' },
        { text: 'Blog', url: '#' },
        { text: 'Contacts', url: '#' },
        ],

        trainings :[
                    {
                        title: "Corsi",
                        
                    },
                    {
                        title: "Mountain Bike",
                       
                    },
                    {
                        title: "Pedalare",
                        
                    },
                    {
                        title: "Pedalare",
                        
                    },
                    ],

        quickLinks: [
                    {
                        title: "Pacchetti",
                        
                    },
                    {
                        title: "Pedalare",
                        
                    },
                    {
                        title: "Pedalare",
                        
                    },
                    {
                        title: "Pedalare",
                        
                    },
                    
]

    }
   }
}
</script>

<template>
    <div class="container">
        <AppHeader :links="navLinks"></AppHeader>
    </div>
    <AppMain></AppMain>
    <AppFooter :trainings="trainings" :quickLinks="quickLinks"></AppFooter>
</template>

<style lang="scss">
@use './styles/general.scss';


</style>