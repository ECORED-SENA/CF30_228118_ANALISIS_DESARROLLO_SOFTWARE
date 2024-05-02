<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 2
      h1 Implantación de sistemas de alta disponibilidad 

    .row
      .col-auto.d-none.d-md-block(style="place-self:center;" data-aos="fade-right")
        figure
          img(src="@/assets/curso/tema2/1.svg")
      .col(style="place-self:center;" data-aos="fade-left")
        p.mb-0 La implantación requiere de algunos lineamientos, independiente de la tecnología de #[em clustering] o de almacenamiento, se centra en que sea servible para las tecnologías actuales y futuras dentro de una organización.  
    
    p.mt-4(data-aos="fade-up") A continuación, conozca las siguientes definiciones: 

    TabsB.color-acento-botones.mt-4
      .py-4.py-md-5(titulo="Definición de objetivos" :icono="require('@/assets/curso/tema2/2.svg')")
        .row.col-xl-11.m-auto
          .col-lg-7.mb-4.mb-lg-0(style="place-self:center;")
            h5 Definición de objetivos 
            p El objetivo es analizar las distintas opciones de alta disponibilidad, y con esto establecer su intencionalidad, según lo que se determine como importante, pero haciendo un análisis de riesgos en sistemas críticos.
            p Para su definición, se deben tener en cuenta elementos como el empleo de contenedores, el almacenamiento redundante, la duplicidad de las redes de telecomunicaciones, la virtualización de sistemas, la operación ininterrumpida y el balanceo de carga.  
          .col-lg-5(style="place-self:center;")
            figure
              img(src='@/assets/curso/tema2/4.png')
      .py-4.py-md-5(titulo="Análisis de opciones de alta disponibilidad" :icono="require('@/assets/curso/tema2/3.svg')")
        .row.col-xl-11.m-auto
          .col-lg-7.mb-4.mb-lg-0(style="place-self:center;")
            h5 Análisis de opciones de alta disponibilidad 
            p Son necesarios varios aspectos al momento de considerar la implementación de un sistema de alta disponibilidad o para adquirirlo desde un proveedor. Por eso se establecen algunos lineamientos, iniciando a partir de los indicadores de nivel de servicio.  
          .col-lg-5(style="place-self:center;")
            figure
              img(src='@/assets/curso/tema2/5.png')
    
    Separador

    .titulo-segundo(data-aos="flip-up")
      h2#t_2_1 2.1  Indicadores de nivel de servicio
    
    p(data-aos="fade-right") El funcionamiento del #[em hardware] sin fallas es la base para dotar a un sistema una alta disponibilidad. Para saber cómo presentar el valor de alta disponibilidad a ofrecer, se debe tener en cuenta la norma IEEE 762/2006 que suministra el método del cálculo de este indicador para sistemas eléctricos, pero es aplicable a todo sistema eléctrico o electrónico. 

    .row.mt-4
      .col-lg-5.mb-4.mb-lg-0(data-aos="fade-right" style="place-self:center;")
        figure.m-auto.col-9.col-md-8.col-lg-12
          img(src="@/assets/curso/tema2/6.png" style="place-self:center;")
      .col-lg-7(data-aos="fade-left")
        .p-4(style="background-color:#ECF2FF;border-radius:12px;")
          p.mb-0 En dicha norma, se mencionan algunos indicadores como lo son: fiabilidad, disponibilidad, tiempo medio entre paradas (MTBF, #[em Mid Time Between failures]), duración de las paradas (MTTR, o #[em Mid Time To Repair]), número de paradas por mantenimiento y tiempo total perdido por mantenimiento. 
        p.mt-4 Para poder realizar este cálculo, se necesita tener registrado en una tabla, un registro por cada parada de los servicios, con los siguientes datos: 
        ul.lista-ul.ps-4
          li 
            i.fas.fa-code(style="color:#8722E2;")
            | Servicio que ha parado. 
          li 
            i.fas.fa-code(style="color:#8722E2;")
            | Motivo de la parada (mantenimiento, actualización, falla, etc.). 
          li 
            i.fas.fa-code(style="color:#8722E2;")
            | Duración de la parada (en minutos o segundos). 
    
    Separador

    .titulo-segundo(data-aos="flip-up")
      h2#t_2_2 2.2  Métodos de cálculos de los indicadores 
    
    p(data-aos="fade-right") A continuación, se describen cuatro métodos de cálculo: 

    .cont_2_1.mt-4
      .cont_2_2.pt-4.pb-4.pt-lg-5.pb-lg-5
        .tarjeta.bg-white.p-4.pt-xl-5
          SlyderA(tipo="b")
            .row.col-xl-11.m-auto
              h4 Disponibilidad
              p Es el cociente entre el tiempo que el sistema está disponible y el tiempo total de paradas de los servicios por servicios de mantenimiento programado y notificado o coordinado con el cliente. Para calcularlo, es necesario conocer el tiempo disponible como resta entre el tiempo total por las paradas de mantenimiento previamente programado y el tiempo por parada no programada. Una vez obtenido se divide el resultado entre el tiempo total del periodo considerado.  
              figure.m-auto.col-12.col-md-12.col-lg-9.mt-4
                img(src='@/assets/curso/tema2/7.svg' alt="La disponibilidad es igual a las horas totales disponibles menos las horas totales de paradas por mantenimiento programado, sobre las horas totales.")
            .row.col-xl-11.m-auto
              h4 Fiabilidad
              p La fórmula es muy parecida a la anterior, con las diferencias que se sustituye en el numerador las horas de parada por mantenimiento por horas de parada por mantenimiento no programado. 
              figure.m-auto.col-12.col-md-12.col-lg-9.mt-4
                img(src='@/assets/curso/tema2/8.svg' alt="La fiabilidad es igual a las horas totales disponibles menos las horas totales de paradas por mantenimiento NO programado, sobre las horas totales.")
            .row.col-xl-11.m-auto
              h4 Tiempo medio entre paradas (#[em TMEP])
              p Es el tiempo medio que ha transcurrido entre dos paradas de mantenimiento, y se requiere para su cálculo en el numerador las horas totales del periodo, y en denominador, el número de paradas.
              figure.m-auto.col-12.col-md-7.col-lg-5.mt-4
                img(src='@/assets/curso/tema2/9.svg' alt="El TMEP es igual a las horas totales del periodo, sobre la cantidad de paradas.")
            .row.col-xl-11.m-auto
              h4 Tiempo medio hasta puesta en marcha (TMPM) 
              p Representa el tiempo medio de duración de las diversas paradas ocurridas en el periodo e ítem analizado. 
              figure.m-auto.col-12.col-md-7.col-lg-5.mt-4
                img(src='@/assets/curso/tema2/10.svg' alt="El TMPM es igual a las horas totales paradas, sobre la cantidad de paradas.")
      
      p.mt-4(data-aos="fade-right") La implantación de sistemas de alta disponibilidad, requiere de un funcionamiento ininterrumpido y para garantizarlo, el #[em hardware] del sistema obligatorio debe exigirle a un sistema una alta disponibilidad, para lo cual es necesario mantenerlo en operación: 

      .pt-0(style="position:relative")
        .semicircle_absolute.d-none.d-md-block(style="left: unset !important;right: -190px !important;top:-45px;")
        .row.mt-4
          .col-lg-3.mb-4.mb-lg-0(data-aos="fade-right" style="place-self:center;")
            figure.m-auto.col-7.col-md-7.col-lg-12
              img(src="@/assets/curso/tema2/11.svg" style="place-self:center;")
          .col-lg-9(data-aos="fade-left")
            AcordionA.acordion1(tipo="a" clase-tarjeta="tarjeta tarjeta--azul")
              .row.col-xl-11.m-auto(titulo="Condiciones ambientales adecuadas ")
                p Para poder tener estas condiciones (temperatura, humedad, circulación de aire), se emplean instalaciones o sitios específicos para ubicar los equipos, donde se centraliza todo el funcionamiento. 
              .row.col-xl-11.m-auto(titulo="Condiciones óptimas de suministro energético ")
                p Para lo cual se suelen emplear técnicas de instalación tales como, duplicar las fuentes de alimentación de los equipos y duplicar los equipos de interconexión, incluyendo cableado.
      p.mt-4(data-aos="fade-right") Además de estas condiciones, es fundamental conocer la integridad, respaldo y los servidores redundantes; a continuación, se relaciona información importante para este proceso: 

      .pt-0(style="position:relative")
        .semicircle_absolute.d-none.d-md-block(style="top:unset !important;bottom: 0 !important;")
        .row.mt-4
          .col-lg-9.mb-4.mb-lg-0(data-aos="fade-right")
            AcordionA.acordion1(tipo="a" clase-tarjeta="tarjeta tarjeta--azul")
              .row.col-xl-11.m-auto(titulo="Integridad y respaldo de los datos")
                p Mediante la integridad de datos, se puede asegurar que no ha sido modificada por terceros. Para garantizar la integridad en los datos almacenados o transmitidos, se emplean técnicas como cifrado o firmas digitales. 
                p Garantizar esto es un poco más difícil, generalmente es algún #[em malware] o alguna función interna de algún sistema operativo que tenga un bache de seguridad. 
                p Sin embargo, existen herramientas para detectar este tipo de vulnerabilidades, como #[em Rootkit Hunger], por citar un ejemplo. 
              .row.col-xl-11.m-auto(titulo="Servidores redundantes ")
                p Se evalúa la aplicación de clúster de servidores, máquinas virtuales o contenedores, y se selecciona la técnica y el número de nodos de acuerdo con las características que se desea dotar al servicio, si estará centrada en el alto desempeño o alta disponibilidad. 
              .row.col-xl-11.m-auto(titulo="Elección de tecnología y/o proveedor de servicio ")
                p De acuerdo al análisis al tipo de nodos (máquinas virtuales, contenedores o equipos físicos), se ha de seleccionar o la tecnología a emplear o el proveedor en la nube que cumpla con las características deseadas. 
                p Muchas veces el costo de licenciamiento o el coste de aprovisionamiento limitan lo deseado, en tal caso se recomienda dimensionar el alcance, pero considerar una estimación del crecimiento de manera que los sistemas se puedan escalar considerando los costes que esto conlleve. 
              .row.col-xl-11.m-auto(titulo="Configuración de servicios y puesta en marcha ")
                p En este punto del plan de implementación, independiente de la tecnología o el proveedor a seleccionar, es de vital importancia considerar el plan de capacitación técnica, de manera que la configuración seleccionada aproveche al máximo o el licenciamiento o el nivel de servicios que se han contratado, de otra forma es posible que se desplieguen con servicios con una configuración estándar o genérica que no explote las características contratadas o adquiridas. 
              .row.col-xl-11.m-auto(titulo="Pruebas de carga ")
                p Las pruebas de carga, miden el rendimiento del #[em software] y siguen dos tipos de procedimientos: 
                ol.lista-ol--cuadro
                  li.d-flex
                    .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                      span.fw-bold(style="color:initial;") a)
                    div #[strong Pruebas de caja negra:] son pruebas sencillas que no se dotan de permisos de usuario para acceder, solo se puede probar lo que externamente se ve de un servicio, sin emplear las credenciales de acceso que permitan acceder a toda funcionalidad. 
                  li.d-flex
                    .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                      span.fw-bold(style="color:initial;") b)
                    div #[strong Pruebas de caja blanca:] interesa verificar internamente las partes que componen un sistema, de manera que debe seguir una secuencia lógica, la primera sería acceder al sistema con credenciales de acceso válidas. 
          .col-lg-3(data-aos="fade-left" style="place-self:center;")
            figure.m-auto.col-7.col-md-7.col-lg-12
              img(src="@/assets/curso/tema2/12.svg" style="place-self:center;")

      p.mt-4(data-aos="fade-right") Se pueden hacer varias pruebas de carga según uno de estos dos métodos: 

      .row.mt-4.justify-content-center
        .col-lg.mb-4.mb-lg-0.col-md-8(data-aos="zoom-in")
          .h-100.p-4.p-lg-5.text-white.text-center(style="background-color:#0B47DB;border-radius:23px;")
            figure.text-center
              img(src="@/assets/curso/tema2/13.svg" style="display:inline;max-width:150px;")
            h5.mt-4 Pruebas reales
            p Con determinado número de usuarios concurrentemente usando las funcionalidades del sistema. 
        .col-lg.mb-4.mb-lg-0.col-md-8(data-aos="zoom-in")
          .h-100.p-4.p-lg-5.text-white.text-center(style="background-color:#0B47DB;border-radius:23px;")
            figure.text-center
              img(src="@/assets/curso/tema2/14.svg" style="display:inline;max-width:150px;")
            h5.mt-4 Pruebas sintéticas
            p Se emplea un sistema o programa especialmente diseñado para tales fines como por ejemplo el sistema JMeter. 
        .col-lg(data-aos="zoom-in-left" data-aos-duration="1800")
          figure.m-auto.col-8.col-md-7.col-lg-12
            img(src="@/assets/curso/tema2/15.svg")
    
    .p-4.mt-4(data-aos="flip-up" style="border:4px #3A1D71 dashed;border-radius:15px;" data-aos-duration="1100")
      p.mb-0 Es recomendable seguir unos lineamientos metodológicos previamente establecidos, y al momento de ser probados, se debe dotar a los sistemas de alta disponibilidad, tanto para servicios locales o servicios a contratar, para que sean desplegados en la nube. 




</template>

<script>
export default {
  name: 'Tema2',
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
<style lang="sass">
.tabs-b__content-item
  background-color: #F7EEFE
.tabs-b__tab.tabs-b__tab--active
  background-color: #f5edfd
.tabs-b__tab
  border-color: #F0C518
.slyder-a__bullets__item
  background-color: #DBBDF5
  border: 0px
.slyder-a__bullets__item--active
  background-color: #A854F3 !important
  border-color: #A854F3 !important
.slyder-a__btn--sigt, .slyder-a__btn--atrs
  background-color: #FFCE00
  border: 1px solid #FFCE00
.cont_2_1, .cont_2_1 *
  position: relative
.cont_2_1:before
  content: ''
  position: absolute
  width: 125%
  left: -15%
  height: 90%
  top: 10%
  background: rgb(236,242,255)
  background: linear-gradient(180deg, rgba(236,242,255,1) 0%, rgba(236,242,255,0.6419817927170868) 80%, rgba(236,242,255,0) 100%)
.cont_2_2, .cont_2_2 *
  position: relative
.cont_2_2:before
  content: ''
  position: absolute
  width: 125%
  left: -15%
  height: 100%
  top: 0
  background: url(../assets/curso/tema1/2.png)
  background-size: 100% 100%
  background-position: center
.acordion1 .tarjeta
  background-color: #3A1D71
  transition: all .3s ease-in
.acordion1 .tarjeta *
  color: #fff
.acordion1 .acordion__accion__btn--a
  background-color: #F0C518
.acordion1 .acordion__accion__btn--a i
  color: #12263F !important;
.acordion1 .tarjeta--azul.acordion__activo
  background-color: #EAD6FC
.acordion1 .tarjeta--azul.acordion__activo *
  color: #12263F !important
.semicircle_absolute
  position: absolute
  width: 300px
  left: -190px
  top: 0
  height: 300px
  border-radius: 50%
  background-color: white
  box-shadow: 0px 0px 35px rgba(0,0,0,.1)
  z-index: 0
@media screen and (max-width: 992px)
  .cont_2_2:before
    background-size: cover !important
</style>
