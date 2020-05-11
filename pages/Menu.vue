<template>
  <q-page class="row q-pa-xl">
    <div class="col-12 q-px-xl">
      <h4 class="q-mx-xl q-mt-none text-blue-grey">Menú</h4>
      <div class="text-body1 q-px-xl text-blue-grey-6">
        Conóce algunos de nuestros pasteles tradicionales, también puedes
        <router-link class="pink-link" to="/contacto">contáctarnos</router-link>
        para personalizar el tuyo.
      </div>
      <div class="row q-px-xl q-my-lg flex flex-center">
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel2.jpg" @click="openImage('pastel2.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel1.jpg" @click="openImage('pastel1.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel3.jpg" @click="openImage('pastel3.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel4.jpg" @click="openImage('pastel4.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel5.jpg" @click="openImage('pastel5.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel6.jpg" @click="openImage('pastel6.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel7.jpg" @click="openImage('pastel7.jpg')" />
        </div>
        <div class="col-3 q-pa-md">
          <q-img class="cursor-pointer" src="~assets/pastel8.png" @click="openImage('pastel8.png')" />
        </div>
        <div class="col-12 text-center q-pa-md">
          <q-btn outline color="pink" label="Ver mas" size="lg" icon="add" />
        </div>
      </div>
    </div>
    <q-dialog maximized v-model="openedModal">
      <q-card class="row" style="background: rgba(0, 0, 0, 0.6);">
        <q-card-section class="col-12 text-center q-px-xl">
          <q-img width="50%" :src="`img/${selectedImage}`" @hide="openedModal = false" />
        </q-card-section>
      </q-card>
    </q-dialog>
  </q-page>
</template>
<script>
export default {
  name: 'PageMenu',
  data: () => ({
    openedModal: false,
    selectedImage: ''
  }),
  methods: {
    openImage (image) {
      this.selectedImage = image
      this.openedModal = true
    }
  }
}
</script>
