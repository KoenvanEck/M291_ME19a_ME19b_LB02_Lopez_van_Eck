<template>
  <div>
    <h1>Warenkorb</h1>
    <table>
      <thead>
      <tr>
        <th>Name</th>
        <th>Anzahl</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="(product, idx) in cart" :key="idx">
        <td>{{ product.name }}</td>
        <td>{{ product.quantity  }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name: 'Cart',
  computed: mapState(['cart'])
}
</script>

<style lang="scss" scoped>
body {
  font-family: 'Gadugi', Helvetica, Arial, sans-serif;
  margin: 10%;
  background-color: #F7F7F7;
}
h1 {
  color: #00b4d8;
}

h2 {
  font-weight: normal;
  color: #494949;
}

th {
  font-weight: bold;
  color: #494949;
}
</style>
