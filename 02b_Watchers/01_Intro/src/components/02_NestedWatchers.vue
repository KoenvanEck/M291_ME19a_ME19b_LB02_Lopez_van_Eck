<template>
  <div class="container">
    <h1>Konzert Tickets</h1>
    <div>
      <h2>{{ product.label }}</h2>
      <h5>CHF {{ product.price }} (CHF {{ discount }} günstiger)</h5>
      <a href="#" @click="updatePrice">Preis reduzieren</a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      discount: 0,
      product: {
        price: 80,
        label: 'Cro Konzert 2022 - Hallenstadion',
      },
    }
  },
  methods: {
    updatePrice(){
      if (this.product.price < 1) return;
      this.product.price--;
    }
  },
  watch: {
    'product.price'(newVal,oldVal){
      this.discount++;
      console.log(`actual(CHF ${newVal}) and old(CHF ${oldVal}) price.`);
    }
  }
}
</script>
<style lang="scss" scoped>
.container {
  margin: 0 auto;
  padding: 30px;
  max-width: 600px;
  font-family: 'Gadugi', Helvetica, sans-serif;
  margin: 0;
}
a {
  display: inline-block;
  background: #e63946;
  border-radius: 10px;
  font-size: 14px;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
}

h1 {
  color: #00b4d8;
}

h2 {
  font-weight: normal;
  color: #494949;
}
</style>
