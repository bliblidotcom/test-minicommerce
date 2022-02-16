<template>
  <div class="home">
    Hello {{name}}
    <br/>
    How are you doing
    <div v-html="name"></div>
    <ProductList msg="Products List Title" param="ok"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductList from '../components/ProductList.vue'

export default {
  name: 'Home',
  components: {
    ProductList
  },
  computed: {
    name () {
      return this.$route.query.name
    }
  }
}
</script>
