<template>
  <v-main class="mx-10 mt-10">
      <h1>Meu teste de avaliação</h1>
      <p>Quando logar usar este acesso.</p>
      <div>
        <strong>Login: </strong>
        <span>admin</span>
      </div>
      <div>
        <strong>Senha: </strong>
        <span>admin123</span>
      </div>

      <v-card width="600" class="mx-auto mt-15 pa-2">
          <h3>Consulte seu CEP</h3>
          <ConsultaCep/>
      </v-card>
  </v-main>
</template>

<script>
import ConsultaCep from '../components/ConsultaCep.vue'
export default {
  components: { ConsultaCep },

}
</script>

<style>

</style>