<template>
  <nav>
    <ul>
      <li><nuxt-link exact to="/">
          <AppLogo />
        </nuxt-link></li>
      <li><nuxt-link to="/restaurants">Restaurants</nuxt-link></li>
    </ul>
    <div v-if="cartCount > 0" class="smallnum">{{ cartCount }}</div>
    <nuxt-link to="/cart">Cart</nuxt-link>
  </nav>
</template>

<script>
import AppLogo from './AppLogo.vue';
import { mapGetters } from 'vuex';
export default {
  components: {
    AppLogo
  },
  computed: {
    ...mapGetters(['cartCount'])
  }
}
</script>

<style lang="scss" scoped>

</style>