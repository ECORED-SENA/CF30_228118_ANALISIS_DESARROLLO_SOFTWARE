<template lang="pug">
#app.app
  Header
  .contenedor-principal
    AsideMenu
    section.seccion-principal(:class="{'seccion-principal--barra-avance-open' : !menuState}")
      router-view
  BarraAvance
  Accesibilidad
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    menuOpen: false,
  }),
  computed: {
    menuState() {
      return this.$store.getters.isMenuOpen
    },
  },
  mounted() {
    this.$aos.init({
      offset: 100,
    })
  },
}
</script>
<style lang="sass">
.banner-interno
  height: 160px
.banner-interno__fondo
  background-image: url(assets/curso/fondo_tema.png) !important
.banner-principal .tarjeta
  background-position: inherit !important
.titulo-principal__numero
  background-color: #00FFDF !important
.curso-main-container > .container
  overflow-x: clip !important
.titulo-segundo:after
  border-left-color: #00FFDF !important
.banner-principal .tarjeta
  background-color: transparent !important
.titulo-principal.color-acento-contenido .titulo-principal__numero span
  color: #12263F !important
.banner-principal-decorativo-1
  animation: float1 2s ease-in-out infinite alternate !important
  top: 42% !important
  right: 75% !important
.banner-principal-decorativo-2
  animation: float1 3s ease-in-out infinite alternate !important
  top: 25% !important
  right: 25% !important
.banner-principal-decorativo-3
  animation: float1 3s ease-in-out infinite alternate !important
  top: 66% !important
  right: 15% !important
.titulo-principal.color-acento-contenido .titulo-principal__numero
  background-color: #00FFDF !important
.cont_titulo_decorativo, .cont_titulo_decorativo *
  position: relative
.cont_titulo_decorativo
  width: fit-content
  margin-bottom: 1.7rem
.cont_titulo_decorativo:before
  content: ''
  position: absolute
  height: 90%
  width: 100%
  left: 0
  bottom: 0
  background-color: #8DEECC
  border-radius: 5px
.banner-principal__row .banner-principal__img
  padding-top: 0rem !important
  padding-bottom: 0rem !important
.banner-principal__row .banner-principal__img img
  max-width: 350px
  margin: 0 auto
@media screen and (max-width: 992px)
  .banner-principal .tarjeta
    background-size: cover !important
</style>
