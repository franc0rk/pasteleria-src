<template>
  <q-page class="row">
    <div class="col-12">
      <q-carousel
        swipeable
        animated
        v-model="slide"
        thumbnails
        infinite
      >
        <q-carousel-slide :name="0" img-src="~assets/banner2.jpg" />
        <q-carousel-slide :name="1" img-src="~assets/banner1.jpg" />
        <q-carousel-slide :name="2" img-src="~assets/banner3.jpg" />
        <q-carousel-slide :name="3" img-src="~assets/banner0.jpg" />
      </q-carousel>
    </div>
    <div class="col-12 q-px-xl">
      <div class="presentation row flex flex-center q-px-xl">
        <div class="col-12 q-px-xl">
          <h4 class="text-center text-blue-grey">Pastelería</h4>
          <div class="text-body1 q-px-xl text-center text-blue-grey-6">
            Somos una pastelería con más de 10 años de experiencia, complaciendo
            y sirviendo a nuestros clientes con opciones personalizadas
            a su gusto y sus necesidades, además de nuestras recetas tradicionales
            ya conocidas por muchos.
            <router-link to="/nosotros" class="pink-link">
              Conóce más acerca de nosotros!
            </router-link>
          </div>
        </div>
      </div>
      <div class="presentation row flex flex-center q-px-xl">
        <div class="col-12 q-px-xl">
          <h5 class="q-mt-xl q-mb-none text-center text-blue-grey">Nuestro menú</h5>
        </div>
      </div>
      <div class="images row q-my-xl flex flex-center">
        <div class="col-4 q-px-md">
          <q-img src="~assets/pastel2.jpg" />
        </div>
        <div class="col-4 q-px-md">
          <q-img src="~assets/pastel1.jpg" />
        </div>
        <div class="col-4 q-px-md">
          <q-img src="~assets/pastel3.jpg" />
        </div>
        <div class="col-12 text-center">
          <router-link to="/menu" class="pink-link cursor-pointer q-mt-md q-mb-none" tag="h5">
            Ver más!
          </router-link>
        </div>
      </div>
      <div class="numbers row flex flex flex-center">
        <div class="col-3 q-px-xs">
          <div class="row">
            <div class="col-12 text-center border-pink q-py-md">
              <q-icon name="store" size="5em" color="pink" />
            </div>
            <div class="col-12 bg-pink text-white text-center text-weight-bold q-py-md">
              <span style="font-size: 3em;">+10</span> años de experiencia
            </div>
          </div>
        </div>
        <div class="col-3 q-px-xs">
          <div class="row">
            <div class="col-12 text-center border-pink q-py-md">
              <q-icon name="mood" size="5em" color="pink" />
            </div>
            <div class="col-12 bg-pink text-white text-center text-weight-bold q-py-md">
              <span style="font-size: 3em;">+100</span> clientes
            </div>
          </div>
        </div>
        <div class="col-3 q-px-xs">
          <div class="row">
            <div class="col-12 text-center border-pink q-py-md">
              <q-icon name="cake" size="5em" color="pink" />
            </div>
            <div class="col-12 bg-pink text-white text-center text-weight-bold q-py-md">
              <span style="font-size: 3em;">+500</span> pasteles horneados
            </div>
          </div>
        </div>
        <div class="col-3 q-px-xs">
          <div class="row">
            <div class="col-12 text-center border-pink q-py-md">
              <q-icon name="palette" size="5em" color="pink" />
            </div>
            <div class="col-12 bg-pink text-white text-center text-weight-bold q-py-md">
              <span style="font-size: 3em;">+200</span> diseños nuevos
            </div>
          </div>
        </div>
      </div>
      <div class="presentation row flex flex-center q-px-xl q-mb-xl">
        <div class="col-12 q-px-xl">
          <h4 class="text-center text-blue-grey">Contáctanos</h4>
          <div class="text-body1 q-px-xl text-center text-blue-grey-6">
            Nuestros teléfonos: <strong>12345678</strong> y <strong>87654321</strong>
          </div>
          <div class="text-body1 q-px-xl text-center text-blue-grey-6">
            Estamos ubicados en: <strong>Calle #123, Colonia, Monterrey, N.L.</strong>
          </div>
          <div class="text-center">
            <router-link to="/contacto" class="pink-link cursor-pointer text-body1 " tag="div">
              Llena nuestro formulario!
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data: () => ({
    slide: 0
  })
}
</script>
<style lang="stylus">
  .q-px-xxl
    padding-left 12em
    padding-right 12em
  .border-pink
    border: 2px solid #e91e63
</style>
