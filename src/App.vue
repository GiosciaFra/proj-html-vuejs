<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'


export default {
   components: {
    AppHeader,
    AppMain
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
</template>

<style lang="scss">
@use './styles/general.scss';


</style>