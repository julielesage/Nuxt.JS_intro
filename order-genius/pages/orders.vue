<template>
  <div>
    <h1 class="display-1">Commander</h1>
    <h2>Available products</h2>
    <div class="card-deck">
      <ProductCard v-for="product in products" :key="product.name" :name=product.name :price="product.price"
        role="order" v-on:order="addProduct">
      </ProductCard>
    </div>
    <h2>Ordered products</h2>
    <div class="card-deck">
      <ProductCard v-for="order in orders" :key="order.name" :name=order.name :price=order.price>
      </ProductCard>
    </div>
  </div>
</template>

<script>
import ProductCard from '../components/ProductCard.vue';

export default {
  name: "orders",
  components: { ProductCard },
  data() {
    return {
      products: [{ name: "pizza", price: 13 }, { name: "frites", price: 3 }, { name: "hot-dog", price: 5 }, { name: "hamburger", price: 8 }],
      orders: []
    };
  },
  methods: {
    addProduct(name, price) {
      this.orders.push({ name, price })
    }
  }

}

</script>

<style scoped>
</style>
