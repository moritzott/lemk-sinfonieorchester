<template>
  <span @click="changeView('AboutView')" >ÜBER</span>
  <span  @click="changeView('NewsView')">NEUIGKEITEN</span>
  <span  @click="changeView('ConcertsView')">KONZERTE</span>
  <span  @click="changeView('ContactView')" >KONTAKT</span>
</template>

<script>
export default {
    name: 'Navigation',
    methods: {
        changeView(newView) {
            this.$parent.$emit('change-view', newView)
        }
    }
}
</script>

<style scoped>
    /* nur bei der Desktop-Ansicht */
    span {
        margin: 0 1em;
        font-size: 18px;
        cursor: pointer;
    }

    /* bei Smartphone und Tablet untereinander! */
    @media only screen and (max-width: 952px) {
        span {
            display: block;
            margin: 1.5em 1em;
            font-size: 18px;
        }
    }

</style>