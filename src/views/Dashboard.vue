<template>
  <v-main class="mx-10 mt-10">
      <h2>Pessoas cadastradas</h2>
      <Tabela :headers="headers" :list="list"/>
  </v-main>
</template>

<script>
import Tabela from '../components/Tabela.vue'
export default {
    components: { Tabela },
    data() {
        return {
            headers: [
                { text: 'Id', align: 'start',value: 'id' },
                { text: 'Nome', align: 'start',value: 'name' },
                { text: 'E-mail', value: 'email' },
                { text: 'Data de nacimento', value: 'dataNacimento' },
                { text: 'Data de Cadastro', value: 'dataCadastro' }
            ],
            list: [
                {
                    id: 1,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2021"
                },
                {
                    id: 2,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2020"
                },
                {
                    id: 3,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2019"
                },
                {
                    id: 4,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2019"
                },
                {
                    id: 5,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2019"
                },
                {
                    id: 6,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2019"
                },
                {
                    id: 7,
                    name: 'Luiz Gabriel',
                    email: "teste@gmail.com",
                    dataNacimento: "10/12/2000",
                    dataCadastro: "10/12/2019"
                },
            ]
        }
    }
}
</script>

<style>

</style>