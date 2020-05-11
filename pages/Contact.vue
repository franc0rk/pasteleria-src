<template>
  <q-page class="row q-pa-xl">
    <div class="col-7 q-px-xl">
      <h4 class="q-mx-xl q-mt-none text-blue-grey">Contacto</h4>
      <div class="text-body1 q-px-xl text-blue-grey-6">
        Acude a nuestra pastelería o contactanos vía telefónica o email.
        Tambien siguenos en nuestras redes sociales para mas información.
        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d14370.830860370848!2d-100.31611324999999!3d25.7802161!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1ses!2smx!4v1587344809859!5m2!1ses!2smx" width="100%" height="250" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
        <br>
        <q-icon class="q-ml-sm" name="location_on" color="pink" /> <span class="text-pink"> Calle #123, Colonia, Monterrey, N.L.</span>
        <br>
        <q-icon class="q-ml-sm" name="phone" color="pink" /> <span class="text-pink"> 12345678</span>
        <br>
        <q-icon class="q-ml-sm" name="mail" color="pink" /> <span class="text-pink"> contacto@pasteleria.com</span>
        <br>
        <q-btn flat icon="fab fa-facebook" round color="pink" />
        <q-btn flat icon="fab fa-instagram" round color="pink" />
      </div>
    </div>
    <div class="col-5 q-mt-xl">
      <h6 class="q-mt-none q-px-xl text-blue-grey-6">
        Llena el siguiente formulario para contactarnos
      </h6>
      <div class="q-px-xl">
        <form>
          <q-select dense color="pink" :options="['Pedido', 'Comentario', 'Información']" label="Motivo del mensaje" v-model="form.subject" />
          <q-input class="q-mt-xs" dense color="pink" v-model="form.name" label="Nombre" />
          <q-input class="q-mt-xs" type="email" dense color="pink" v-model="form.email" label="Email" />
          <q-input class="q-mt-xs" dense color="pink" v-model="form.phone" label="Teléfono" />
          <q-input class="q-mt-xs" dense type="textarea" color="pink" v-model="form.message" label="Mensaje" />
          <q-btn class="q-mt-sm" color="pink" icon="send" label="Enviar" />
        </form>
      </div>
    </div>
  </q-page>
</template>
<script>
export default {
  name: 'PageContact',
  data: () => ({
    form: {
      subject: '',
      name: '',
      email: '',
      phone: '',
      message: ''
    }
  })
}
</script>
