<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-pink text-white">
        <q-btn
          flat
          dense
          round
          icon="cake"
          aria-label="Menu"
          @click="goHome"
        />

        <q-toolbar-title>
          Pastelería
        </q-toolbar-title>

        <div>
          <router-link class="menu-link" to="/nosotros">Nosotros</router-link>
          <router-link class="menu-link" to="/menu">Menú</router-link>
          <router-link class="menu-link" to="/contacto">Contacto</router-link>
        </div>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
    <footer class="bg-pink text-white q-px-xl q-py-md">
      <div class="text-body1">Pastelería 2020. Todos los derechos reservados.</div>
    </footer>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink'

export default {
  name: 'MainLayout',
  methods: {
    goHome () {
      this.$router.push('/')
    }
  }
}
</script>
<style lang="stylus">
  .menu-link
    color white
    margin-right 2em
    text-decoration none
    font-weight bold
  .menu-link:hover
    color black
</style>
