<template>
  <div>
    <Banner />
    <div class="main-container">
      <h1>Monte o seu pedido</h1>
      <OrderForm />
    </div>
  </div>
</template>

<script>
import Banner from '../components/Banner.vue'
import OrderForm from '../components/OrderForm.vue'

export default {
  components: {
    Banner,
    OrderForm
  }
}
</script>