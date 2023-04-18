<template>
  <div class="header-top container d-flex justify-content-between align-content-center py-3">
  <img src="../assets/img/dc-logo.png" alt="dc-logo">
  <ul class="d-flex list-item-none align-items-center text-uppercase">
    <li class="p-3" v-for="(button,index) in navbar" :key="index">
      <a :href="button.url" :class="{'active': button.current}">{{ button.name }}</a>
    </li>
  </ul>
  </div>
  <div class="header-bottom">
  </div>


</template>

<script>
import { headerButtons } from '../data/data';

export default {
  name: 'AppHeader',
  data() {
    return {
      navbar: headerButtons
    }
  }
}
</script>

<style lang="scss" scoped>
.header-bottom {
  width: 100%;
  height: 300px;
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
}

li {
  list-style: none;
  }

a {
  text-decoration: none;
  color: grey
}
a:hover {
  color: #0082F9;
  padding-bottom: 56px;
  border-bottom: 10px solid #0082F9;
}
</style>