<template>
  <v-card width="600" class="mx-auto my-auto pa-3" >
      <h2 class="mb-5">Sejá bem vindo</h2>
      <v-form>
        <v-text-field
            v-model="formData.login"
            outlined
            dense
            label="Login"
        />
        <v-text-field
            v-model="formData.senha"
            outlined
            dense
            label="Senha"
            :type="showSenha ? 'password' : 'text'"
            :append-icon="showSenha ? 'mdi-eye' : 'mdi-eye'"
            @click:append="showSenha = !showSenha"
        />
    </v-form>
    <dir class="py-0" style="color:red">{{mensagem}}</dir>
    <div class="d-flex">
        <v-btn
            @click="logar(formData)"
            color="primary"
        >Logar
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn color="primary" text>
            Esqueci minha senha
        </v-btn>
    </div>
  </v-card>
</template>

<script>
export default {
    data() {
        return {
            formData: {
                login: null,
                senha: null
            },
            showSenha: true,
            mensagem: null
        }
    },
    methods: {
        logar(formData) {
            if (formData.login == "admin" && formData.senha == "admin123") {
                this.$router.push('/dashboard')
            } else {
                this.mensagem = "Usuário ou senha inválido!"
            }
        }
    }
}
</script>

<style>

</style>