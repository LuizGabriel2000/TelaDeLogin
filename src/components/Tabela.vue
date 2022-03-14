<template>
  <v-data-table
    :headers="headers"
    :items="list"
    :items-per-page="5"
    class="elevation-1 mt-10"
  ></v-data-table>
</template>

<script>
export default {
    props: {
        headers: Array,
        list: Array
    }
}
</script>

<style>

</style>