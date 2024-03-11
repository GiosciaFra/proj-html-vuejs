<script>
import AppHeader from './components/AppHeader.vue'


export default {
   components: {
    AppHeader,
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
</template>

<style lang="scss">
@use './styles/general.scss';


</style>