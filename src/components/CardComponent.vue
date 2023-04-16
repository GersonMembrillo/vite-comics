<template>
  <div class="col-12 col-lg-2 my-4">
    <div class="card border-0">
      <div class="card-body p-0">
        <div class="card-image">
          <img :src="image" :alt="title" class="img-fluid">
        </div>
        <div class="card-title text-uppercase text-white bg-dark mb-0 pt-2">
          {{ title }}
        </div>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: 'CardComponent',
  props: ['image','title'],
}
</script>

<style lang="scss" scoped>

.img-fluid {
  width: 100%;
  height: 150px;
  object-fit: cover;
  object-position: top;
}
</style>