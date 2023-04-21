<template>
<div class="main-top py-3 bg-dark position-relative">
  <div class="container">
    <div class="row">
      <CardComponent :image="card.thumb" :title="card.series" v-for="(card,index) in cards" :key="index" />
    </div>
  </div>
  <div class="d-flex justify-content-center">
    <button type="button" class="btn btn-primary d-flex rounded-0">LOAD MORE</button>
  </div>

</div>
<div class="main-bottom p-5">
  <div class="container">
    <ul class="d-flex list-unstyled row-cols-5 mb-0">
      <li class="" v-for="(button, index) in buttons" :key="index">
        <a class="text-decoration-none text-white d-flex justify-content-center align-items-center" :href="button.url" :class="{ 'active': button.current }">
          <img class="bottom-img pe-2" :src="button.src" :alt="button.name">
          <p class="mb-0 text-uppercase">{{ button.name }}</p>
        </a>
      </li>
    </ul>
  </div>

</div>
</template>

<script>
import { mainCards } from '../data/data'
import CardComponent from './CardComponent.vue';
import { mainButtons } from '../data/data';

export default {
    name: "AppMain",
    components: {
        CardComponent
    },
    data() {
        return {
          cards: [...mainCards],
          buttons: [...mainButtons],

        };
    },
}
</script>

<style lang="scss" scoped>
.main-bottom{
  background-color: #0082F9;
  .bottom-img{
    width: auto;
    height: 50px;
  }
}
</style>