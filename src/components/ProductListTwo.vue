<template>
  <div id="product-list-two">
    <h2>Product List Two with getters from store</h2>
    <ul>
      <li v-for="product in allProducts">
        <span class="name">
          {{ product.name }}
        </span>
        <span class="price">
          ${{ product.price }}
        </span>
      </li>
    </ul>

  </div>
  
</template>

<script>
export default {
  computed: {
    allProducts() {
      return this.$store.getters.productsList
    }
  }
}
</script>

<style scoped>
#product-list-two {
  padding: 0.8rem 1.2rem;
  margin-bottom: 1.8rem;
  background-color: #d1e4ff;
  box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
}

#product-list-two ul {
  padding: 0;
  list-style-type: none;
}

#product-list-two li {
  margin-right: 0.8rem;
  margin-top: 0.8rem;
  padding: 1.8rem;
  background: rgba(255,255,255,0.7);
}

.price{
  font-weight: bold;
  color: #aa0ce8;
  display: block;
}
</style>