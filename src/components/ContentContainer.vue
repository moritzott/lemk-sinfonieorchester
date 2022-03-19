<template>
    <!-- content of the page -->
  <div class="content-of-page">
    <!-- Banner image -->
    <Banner />
    <!-- the specific content of the page -->
    <component :is="viewname" />
  </div>
</template>

<script>
// import the views / sites (remember: here they are called views, but the app 
// does not use the router. so technically they are just components)
import AboutView from '../views/AboutView.vue'
import ConcertsView from '../views/ConcertsView.vue'
import ContactView from '../views/ContactView.vue'
import NewsView from '../views/NewsView.vue'

import Banner from './Banner.vue'

export default {
    props: [
        'viewname'
    ],
    
    components: {
        AboutView,
        ConcertsView,
        ContactView,
        NewsView,
        Banner
    },
    methods: {
        changeView(viewname){
            this.view = viewname
        }
    }
}
</script>

<style>

</style>