<template>
  <div class="card text-white bg-dark mb-3" style="max-width: 18rem;">
    <div class="card-header">{{ name }}</div>
    <div class="card-body">
      <p class="card-text">{{ price }}</p>
      <button v-if="role === 'order'" @click="$emit('order', name, price)">ADD</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  props: ["name", "price", "role"]
}
</script>
