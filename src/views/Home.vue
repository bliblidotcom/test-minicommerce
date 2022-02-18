<template>
  <div class="home">
    Hello {{name}}
    <br/>
    How are you doing
    <span v-html="name"></span>?
    <br/>
    I'm good <span v-html="code"></span>.
    <br/>
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
    },
    code () {
      return this.$route.params.code
    }
  }
}
</script>
