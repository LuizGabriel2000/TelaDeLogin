<template>
  <v-row class="ma-0">
      <v-col cols="6">
          <v-text-field
            v-model="cep"
            outlined
            dense
            label="CEP"
            v-mask="'#####-###'"
        />
      </v-col>
      <v-col cols="6">
          <v-btn 
            color="primary"
            @click="buscar(cep)"
          >
              Buscar
          </v-btn>
      </v-col>
      <v-col cols="6">
        <strong>{{dados.logradouro}}</strong>  
      </v-col>
      <v-col cols="6">
          <strong>{{dados.bairro}}</strong>
      </v-col>
      <v-col cols="6">
          <strong>{{dados.localidade}}</strong>
      </v-col>
      <v-col cols="6">
          <strong>{{dados.uf}}</strong>
      </v-col>
  </v-row>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            cep: "",
            dados: {
                logradouro: null,
                bairro: null,
                localidade: null,
                uf: null
            }
        }
    },
    methods: {
        buscar(cep) {
            console.log(cep)
            axios.get(`https://viacep.com.br/ws/${cep}/json`).then(response => {
                this.dados = response.data
            })
        }
    }
}
</script>

<style>

</style>