<script>


export default {
    name: 'AppHeader',
}
</script>

<template>
    <div class="container">
        <nav class="navbar">
            <div id="logo">

                <img src="/public/img/logo-gobike.png" alt="Logo" class="logo">
            </div>

            <div id="links">

                <ul class="nav-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Trainings</a></li>
                    <li><a href="#">Packages</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Contacts</a></li>
    
                </ul>
            </div>

            <div id="right-nav">

                icon hamb

                <button>
                    Upcoming Events
                </button>


            </div>


        </nav>
    </div>
</template>

<style lang="scss">
@use '../styles/general.scss';


</style>