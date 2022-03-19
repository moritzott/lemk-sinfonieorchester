<template>
  <!-- the header -->
  <header>
    <div class="header-container">
      <!-- Name of the App -->
      <span class="name-of-app">Lemker Sinfonieorchester</span>
      <!-- Burger Menu -->
      <span @click="openMobileNavbar" class="burger-menu-sign">&#9776;</span>
      <!-- Navbar -->
      <NavbarDesktop @change-view="changeView" />
      <!-- Mobile Navbar as Modal -->
      <NavbarMobileModal @change-view="changeView" />
    </div>
  </header>

  <!-- The specific Content of the page(s) -->
  <ContentContainer :viewname="viewname" />

  

</template>

<script>

// import components:
import NavbarDesktop from './components/NavbarDesktop.vue'
import NavbarMobileModal from './components/NavbarMobileModal.vue'
import ContentContainer from './components/ContentContainer.vue'

export default {
  name: 'App',
  data() {
    return {
      viewname: 'AboutView'
    }
  },
  components: {
    NavbarDesktop,
    NavbarMobileModal,
    ContentContainer
  },
  methods: {
    changeView(newView) {
      this.viewname = newView
    },

    openMobileNavbar() {
      // console.log('ICh war hier');
      const navbarModal = document.querySelector('.modal-navbar');
      navbarModal.style.display = 'block';
    },
  }
}
</script>

<style>
/* Import the Fonts css file */
@import './assets/css/fonts.css';

/* Import the global css file */
@import './assets/css/global.css';

nav span {
  text-decoration: none;
  color: black;
  text-transform: uppercase;
}

nav span:hover {
  border-bottom: 2px solid black;
}

@media only screen and (max-width: 952px) {
      nav span {
          border: none;
      }

      nav span:hover {
          border-bottom: none;
          color: rgb(77, 73, 73);
      }
  }
</style>
