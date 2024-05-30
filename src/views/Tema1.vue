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
        p.mb-0 Para conocer sobre gestión de redundancia y alta disponibilidad, es importante identificar que la primera se centra en la capacidad de interconectar los #[em data centers] en caso de que el principal falle, mientras que la alta disponibilidad se centra en la capacidad de tener operando los sistemas sin interrupción. En ocasiones, se ofrecen servicios de alta disponibilidad (HA, de inglés #[em High Availability]) y para ello, es indispensable iniciar con el #[em backup] de los datos, porque la alta disponibilidad no conlleva copia de la información.  
    
    p.mt-4(data-aos="fade-up") A continuación, se profundizará en estos conceptos: 

    .cont_1_1.mt-4
      .cont_1_2.pt-4.pb-4.pt-lg-5.pb-lg-5
        .tarjeta.bg-white.p-4.pt-xl-5
          SlyderA(tipo="b")
            .row.col-xl-11.m-auto
              .col-lg-7.mb-4.mb-lg-0(style="place-self:center;")
                h4 Redundancia de #[em hardware]
                p Hace referencia a tener un componente del sistema duplicado. En esta instancia, se puede considerar que los proveedores de servicios en la nube tienen todos esos servicios, que ofrecen operando dentro de Centros de #[em Procesos de Datos] (CPD) o más conocidos como #[em Data Centers], y las máquinas en algún momento terminan fallando, porque tienen un tiempo de vida estimado muy difícil de garantizar. 
                p Su objetivo no es evitar fallas, sino que no afecten a los usuarios. La forma de lograr esto, es duplicando el dispositivo de manera que cuando falle la máquina los servicios que dependen de ese #[em hardware], sean trasladados de forma automática a un dispositivo que no esté afectado, de tal forma que cuando dos dispositivos están publicados, se puede decir que están redundados. 
              .col-lg-5(style="place-self:center;")
                figure.m-auto.col-7.col-md-5.col-lg-12
                  img(src='@/assets/curso/tema1/3.png' alt="")
            .row.col-xl-11.m-auto
              .col-lg-7.mb-4.mb-lg-0(style="place-self:center;")
                h4 Alta Disponibilidad: HA (#[em High Availability])
                p Son las características que tiene una arquitectura tecnológica y que determina el grado con el que los servicios TI están activos, es decir, disponibles, para ser usados por el cliente final. La alta disponibilidad garantiza que los sistemas estén disponibles a pesar de que existan fallos en las tecnologías que los soportan. 
              .col-lg-5(style="place-self:center;")
                figure.m-auto.col-7.col-md-5.col-lg-12
                  img(src='@/assets/curso/tema1/4.png' alt="")
            .row.col-xl-11.m-auto
              .col-lg-7.mb-4.mb-lg-0(style="place-self:center;")
                h4 Operación de los servicios 
                p La alta disponibilidad puede ser de dos formas, para poder mantener en operación los servicios:  
                p #[strong Activo-Activo:] ambos equipos, dispositivos o sistemas, están funcionando simultáneamente y generalmente se están repartiendo la carga de trabajo entre ellos. 
                p #[strong Activo-Pasivo:] solo uno de los dispositivos o servicios está en operación, mientras que el segundo equipo, solamente entra en operación, cuando el primero se ha “caído” o no está disponible. En este caso es posible utilizar una copia existente (de un momento determinado de tiempo) de los datos. 
              .col-lg-5(style="place-self:center;")
                figure.m-auto.col-7.col-md-5.col-lg-12
                  img(src='@/assets/curso/tema1/5.png' alt="")
      p.mt-4(data-aos="fade-right") Como se puede inferir, para tener HA se debe tener como mínimo dos sistemas o dispositivos y ambos con idénticos sistemas y características; generalmente se aplica HA a servidores de aplicaciones y a sistemas gestores de base de datos. 
      .pt-0(style="position:relative")
        .semicircle_absolute.d-none.d-md-block(style="left: unset !important;right: -190px !important;top:-45px;")
        .col-lg-10.m-auto.mt-4
          .p-4(style="background-color:#8722E2;border-radius:14px;" data-aos="zoom-in")
            .row
              .col-auto.d-none.d-md-block(style="place-self:center;" data-aos="fade-right")
                figure
                  img(src="@/assets/curso/tema1/6.svg")
              .col(style="place-self:center;" data-aos="fade-left")
                p.text-white.mb-0 En conclusión, el término #[strong redundancia], está vinculado a la implementación de #[strong alta disponibilidad], específicamente mediante la implantación de al menos un dispositivo adicional que se empleará como respaldo (según el modelo activo-pasivo) o balanceador de carga (en el caso activo-activo). 
        
        Separador

      .titulo-segundo(data-aos="flip-up")
        h2#t_1_1 1.1  Clústeres
      
      p(data-aos="fade-right") Cuando la HA es activo-activo, se puede tener mejor desempeño al existir balanceo de cargas, a este tipo de agrupación se le denomina clúster, que es el nombre que se le da a un sistema compuesto de más de una unidad de procesamiento, que trabajan de manera unificada con el mismo objetivo. Estas máquinas tienen en común que realizan las mismas tareas, debido a que tienen una similitud en la configuración y los sistemas informáticos, de manera que pueden trabajar de forma simultánea. 

      .row.mt-4
        .col-lg-5.mb-4.mb-lg-0(data-aos="fade-right" style="place-self:center;")
          figure.m-auto.col-9.col-md-8.col-lg-12
            img(src="@/assets/curso/tema1/7.png" style="place-self:center;")
        .col-lg-7(data-aos="fade-left")
          p La técnica del clúster se puede aplicar a: 
          ol.lista-ol--cuadro.ps-4
            li 
              .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                span.fw-bold(style="color:initial;") 1
              | Máquinas virtuales. 
            li.d-flex
              .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                span.fw-bold(style="color:initial;") 2
              div #[em Containers].
            li 
              .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                span.fw-bold(style="color:initial;") 3
              | Arquitectura de computación. 
            li 
              .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                span.fw-bold(style="color:initial;") 4
              | Redes.
            li 
              .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                span.fw-bold(style="color:initial;") 5
              | Computación en la nube. 
            li 
              .lista-ol--cuadro__vineta(style="background-color:#00FFDF;")
                span.fw-bold(style="color:initial;") 6
              | Banco de datos.
          p.mb-0 El funcionamiento del clúster requiere conocer el concepto llamado “nodo”, el cual es el nombre que atribuye a cada computador o unidad de procesamiento (máquina virtual o contenedor) agregado a un clúster, ya sea virtual o físico. Cuando se hace referencia a las tecnologías o herramientas necesarias para implementar los clústeres, se habla de #[em clustering]. 
      .pt-4(style="position:relative")
        .semicircle_absolute.d-none.d-md-block
        .row.mt-0.mt-md-4
          .col-lg-9.mb-4.mb-lg-0(style="place-self:center;" data-aos="fade-right")
            .p-4(style="background-color:#D6E1FD;border-radius:14px;")
              .row
                .col-auto.d-none.d-md-block(style="place-self:center;" )
                  figure
                    img(src="@/assets/curso/tema1/8.svg")
                .col(style="place-self:center;")
                  p.mb-0 En un clúster los nodos se interconectan gracias a una tecnología o infraestructura de red, generalmente una ya conocida por la empresa, pensando en la facilidad de mantenimiento y control de los costos. Es así, como cada nodo desempeña la misma función que los demás nodos, siendo posible suprimir o adicionar nuevos cuando sea necesario, aún si el clúster se mantiene en funcionamiento sin interrupciones, de tal forma que estas operaciones de agregar o quitar no perjudican el proceso, porque las tareas se distribuyen automáticamente, sin ocasionar problemas.
            p.mt-4 Para que el sistema sea escalable es importante saber que no existe límite de nodos que se puedan operar en un solo clúster y esto es muy importante cuando las empresas están en proceso de crecimiento continuo.  
            p Básicamente, existen dos tipos de clúster o motivos por los que se configuran los clústeres: 
          .col-lg-3.d-none.d-md-block(data-aos="fade-left" style="place-self:center;")
            figure.m-auto.col-7.col-md-6.col-lg-12
              img(src="@/assets/curso/tema1/9.png" style="place-self:center;")
      .row.mt-4
        .col-lg-3.mb-4.mb-lg-0.d-none.d-md-block(data-aos="fade-right" style="place-self:center;")
          figure.m-auto.col-7.col-md-7.col-lg-12
            img(src="@/assets/curso/tema1/10.png" style="place-self:center;")
        .col-lg-9(data-aos="fade-left")
          AcordionA.acordion1(tipo="a" clase-tarjeta="tarjeta tarjeta--azul")
            .row.col-xl-11.m-auto(titulo="Clúster de alto desempeño (<em>High Performance Computing Cluster</em>)")
              p Se utiliza cuando el objetivo es resolver problemas que requieren de mucho procesamiento concurrente, es decir, simultáneo, permitiendo realizarlos en un tiempo útil y de manera que satisfaga la expectativa del usuario. Para lograr esto se hace uso de la técnica de balanceo de carga (#[em Load Balancing]), que consiste en repartir las tareas de manera similar o equilibrada (balanceada) entre los nodos.
            .row.col-xl-11.m-auto(titulo="Clúster de alta disponibilidad (<em>High Availability Computing Cluster</em>)")
              p Su principal objetivo es mantener el sistema en funcionamiento, es decir, está centrado en saber responder automáticamente a fallos sin afectar la continuidad de la prestación del servicio. Para esto, es necesario dotar al clúster de herramientas, control y monitoreo de fallas en la interconexión o en los nodos, redundancia de sistemas, sistemas sustitutos o de respaldo, entre otros. 
    
    Separador

    .titulo-segundo(data-aos="flip-up")
      h2#t_1_2 1.2  Ventajas de la gestión de redundancia y alta disponibilidad
    
    p(data-aos="fade-right") Existen varios motivos por lo que es importante la gestión de la redundancia y alta disponibilidad; a continuación, se relacionan los más representativos que contribuyen a adopción de estrategias para su gestión: 

    .cont_1_3.mt-4
      .row
        .col-lg-3.mb-4.mb-lg-0.col-md-6(data-aos="zoom-in")
          .h-100.cont_1_4.p-4.text-center
            figure.m-auto.text-center
              img(src="@/assets/curso/tema1/11.svg" style="max-width:150px;display:inline;")
            h5.mt-4 Eliminación de fallos 
            p Al ocurrir fallos en el #[em hardware], en las redes, energía o de nivel físico, quedan resueltos de forma automática, debido a que las funciones son trasladadas a nodos no afectados. 
        .col-lg-3.mb-4.mb-lg-0.col-md-6(data-aos="zoom-in")
          .h-100.cont_1_4.p-4.text-center
            figure.m-auto.text-center
              img(src="@/assets/curso/tema1/12.svg" style="max-width:150px;display:inline;")
            h5.mt-4 Recuperación automática 
            p No requiere de la intervención humano–máquina, para que los sistemas se restablezcan o se reconfiguren, para salvaguardar los fallos. 
        .col-lg-3.mb-4.mb-lg-0.col-md-6(data-aos="zoom-in")
          .h-100.cont_1_4.p-4.text-center
            figure.m-auto.text-center
              img(src="@/assets/curso/tema1/13.svg" style="max-width:150px;display:inline;")
            h5.mt-4 Rendimiento
            p Estas arquitecturas permiten que la empresa pueda crecer en operaciones y que los sistemas tecnológicos escalen las necesidades crecientes. 
        .col-lg-3.mb-4.mb-lg-0.col-md-6(data-aos="zoom-in")
          .h-100.cont_1_4.p-4.text-center
            figure.m-auto.text-center
              img(src="@/assets/curso/tema1/14.svg" style="max-width:150px;display:inline;")
            h5.mt-4 Seguridad
            p Se puede garantizar el almacenamiento y disponibilidad de la información. 
             




      
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
<style lang="sass">
.cont_1_1, .cont_1_1 *
  position: relative
.cont_1_1:before
  content: ''
  position: absolute
  width: 125%
  left: -15%
  height: 90%
  top: 10%
  background: rgb(236,242,255)
  background: linear-gradient(180deg, rgba(236,242,255,1) 0%, rgba(236,242,255,0.6419817927170868) 80%, rgba(236,242,255,0) 100%)
.slyder-a__bullets__item
  background-color: #DBBDF5
  border: 0px
.slyder-a__bullets__item--active
  background-color: #A854F3 !important
  border-color: #A854F3 !important
.slyder-a__btn--sigt, .slyder-a__btn--atrs
  background-color: #FFCE00
  border: 1px solid #FFCE00
.cont_1_2, .cont_1_2 *
  position: relative
.cont_1_2:before
  content: ''
  position: absolute
  width: 125%
  left: -15%
  height: 100%
  top: 0
  background: url(../assets/curso/tema1/2.png)
  background-size: 100% 100%
  background-position: center
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
.cont_1_3, .cont_1_3 *
  position: relative
.cont_1_3:before
  content: ''
  position: absolute
  width: 125%
  left: -15%
  height: 100%
  bottom: -28%
  background: url(../assets/curso/tema1/15.png)
  background-size: 100% 100%
  background-position: center
.cont_1_4, .cont_1_4 *
  position: relative
.cont_1_4:before
  content: ''
  position: absolute
  height: 80%
  left: 0
  background-color: #fff
  width: 100%
  bottom: 0
  border-radius: 20px
  box-shadow: 0px 5px 30px rgba(0,0,0,.09)
@media screen and (max-width: 992px)
  .cont_1_2:before, .cont_1_3:before
    background-size: cover !important
</style>
