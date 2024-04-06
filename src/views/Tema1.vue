<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 1
      h1 Gestión de redundancia y alta disponibilidad

    .row
      .col-auto.d-none.d-md-block(style="place-self:center;" data-aos="fade-right")
        figure
          img(src="@/assets/curso/tema1/1.svg")
      .col(style="place-self:center;" data-aos="fade-left")
        p Para conocer sobre gestión de redundancia y alta disponibilidad, es importante identificar que la primera se centra en la capacidad de interconectar los #[em data centers] en caso que el principal falle, mientras que la alta disponibilidad se centra en la capacidad de tener operando los sistemas sin interrupción. En ocasiones, se ofrecen servicios de alta disponibilidad (HA, de inglés #[em High Availability]) y para ello, es indispensable iniciar con el #[em backup] de los datos, porque la alta disponibilidad no conlleva copia de la información.  
    
    p.mt-4(data-aos="fade-up") A continuación, se profundizará en estos conceptos: 

      
</template>

<script>
export default {
  name: 'Tema1',
  components: {},
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>
<style lang="sass"></style>
