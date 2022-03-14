<template>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <h2 class="d-flex align-center">
        <v-btn icon @click="$router.push('/')">
          <v-icon>mdi-home</v-icon>
        </v-btn>
        Teste de avaliação
      </h2>

      <v-spacer></v-spacer>

      <v-btn
        text
        @click="$router.push('/login')"
      >
        <v-icon>mdi-account</v-icon>
        <span class="mr-2">Logar</span>
      </v-btn>
    </v-app-bar>
</template>

<script>
export default {

}
</script>

<style>

</style>