<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    .cont_intro1.pb-5
      .row
        .col-lg-7.mb-4.mb-lg-0(data-aos="fade-right" style="place-self:center;")
          .p-4.p-lg-5.h-100.text-white(style="background-color:#3A1D71;border-radius:22px;")
            p.mb-0 En el momento de contratar u ofrecer servicios en la nube, seguramente se debe asesorar o recibir el asesoramiento sobre un conjunto de características o configuraciones que permiten garantizar con mayor seguridad, la operación de los servicios que se van a contratar. No solo se trata de garantizar el almacenamiento de la información, sino la de aquellos servicios que la publican y la procesan. 
        .col-lg-5(data-aos="fade-left" style="place-self:center;")
          figure.m-auto.col-12.col-md-8.col-lg-12
            img(src="@/assets/curso/intro2.png")
      .row.mt-4
        .col-auto.d-none.d-md-block(style="place-self:center;" data-aos="fade-right")
          figure
            img(src="@/assets/curso/intro3.svg")
        .col(style="place-self:center;" data-aos="fade-left")
          p El presente componente formativo, le permitirá conocer los conceptos relacionados con procesos de gestión de la redundancia y alta disponibilidad, de forma que se comprenda el contexto de los servicios que se ofrecen, y a su vez, también se trabajará la temática de la implantación de sistemas de alta disponibilidad. 
          p.mb-0 #[strong(style="color:#8722E2;") Bienvenido.]

    
    
</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
}
</script>
<style lang="sass">
.cont_intro1, .cont_intro1 *
  position: relative
.cont_intro1:before
  content: ''
  position: absolute
  width: 125%
  left: -15%
  height: 100%
  top: 0
  background: url(../assets/curso/intro1.png)
  background-size: 100% 100%
  background-position: center
@media screen and (max-width: 992px)
  .cont_intro1:before
    background-size: cover !important
</style>
