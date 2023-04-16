<template>
<div class="main-top py-3 bg-dark">
  <div class="container">
    <div class="row">
      <CardComponent :image="card.thumb" :title="card.series" v-for="(card,index) in cards" :key="index" />
    </div>
  </div>
</div>
<div class="main-bottom p-5">
  <div class="container">
    <ul class="d-flex list-unstyled row-cols-5">
      <li class="" v-for="(button, index) in buttons" :key="index">
        <a class="text-decoration-none text-white" :href="button.url" :class="{ 'active': button.current }">
          <img :src="button.image" alt="">
          {{ button.name }}
        </a>
      </li>
    </ul>
  </div>

</div>
</template>

<script>
import { mainCards } from '../data/data'
import CardComponent from './CardComponent.vue';
import { mainButtons } from '../data/data.js';

export default {
    name: "AppMain",
    components: {
        CardComponent
    },
    data() {
        return {
          cards: [...mainCards],
          buttons: mainButtons,

        };
    },
}
</script>

<style lang="scss" scoped>
.main-bottom{
  background-color: #0082F9;
}
</style>