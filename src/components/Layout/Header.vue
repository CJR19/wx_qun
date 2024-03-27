<template>
  <div class="header">
    <div class="header__nav">
      <router-link
        v-for="route in props.routes"
        :key="route.path"
        :to="route.path"
        class="nav__item"
        :class="{ 'nav__item--active': $route.path === route.path }"
      >
        {{ route.name }}
      </router-link>
    </div>
  </div>
</template>
  
<script setup lang='ts'>
import { defineProps,ref } from 'vue'
interface Route {
  path: string;
  name: string;
}
const props = defineProps({
  routes: Array<Route>
})

</script>
  
<style lang="scss" scoped>

$themColor: green;
  
  .header {
    width: 100%;
    height: 50px;
    background-color: #333;

    &__nav {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
      color: #fff;

      .nav__item {
        height: 100%;
        margin: 0 10px;
        color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        
        &--active {
          color: $themColor;
          border-bottom: 3px solid $themColor;
        }
      }
    }
  }

</style>