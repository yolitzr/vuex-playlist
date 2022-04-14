<template>
  <div id="product-list-one">
    <h2>Product List One with mapGetters</h2>
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
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters({
      allProducts: 'productsList'
    })
  }
}
</script>

<style scoped>
#product-list-one {
  padding: 0.8rem 1.2rem;
  margin-bottom: 1.8rem;
  background-color: #fff8b1;
  box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
}

#product-list-one ul {
  padding: 0;
  list-style-type: none;
}

#product-list-one li {
  display: inline-block;
  margin-right: 0.8rem;
  margin-top: 0.8rem;
  padding: 1.8rem;
  background: rgba(255,255,255,0.7);
}

.price{
  font-weight: bold;
  color: #E8800C;
}
</style>