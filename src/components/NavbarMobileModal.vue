<template>
    <div @click="closeMobileNavbar" id="modalNavbar" class="modal-navbar">
        <div class="modal-navbar-content">
            <div class="close-button">
                <span>&times;</span>
            </div>
            
            <nav>
                <Navigation />
            </nav>
        </div>
    </div>
</template>

<script>
import Navigation from './Navigation.vue'

export default {
    methods: {
        closeMobileNavbar() {
            const navbarModal = document.querySelector('.modal-navbar');
            navbarModal.style.display = 'none';
      }
    },
    components: {
        Navigation
    }
}
</script>

<style scoped>
    .close-button {
        text-align: right;
        margin-top: 1em;
    }
    span {
    /* margin-top: 2em; */
    font-size: 40px;
    /* float: right; */
    cursor: pointer;
    /* display: block; */
    /* margin-bottom: 2em; */
    }

</style>