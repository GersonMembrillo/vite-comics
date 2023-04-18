<template>
  <div class="top-footer position-relative">
    <div class="container d-flex py-5">
      <div>
        <ul class="ps-0">
          <h3>DC Comics</h3>
          <li v-for="index in buttonsComics" :key="index">
          <a href="#">{{ index }}</a>
        </li>
        </ul>
        <ul class="ps-0">
          <h3>Shop</h3>
          <li v-for="index in buttonsShop" :key="index">
            <a href="#">{{ index }}</a>
          </li>
        </ul>
      </div>
      <ul>
        <h3>DC</h3>
        <li v-for="index in buttonsDC" :key="index">
          <a href="#">{{ index }}</a>
        </li>
      </ul>
      <ul>
        <h3>Sites</h3>
        <li v-for="index in buttonsSites" :key="index">
          <a href="#">{{ index }}</a>
        </li>
      </ul>
    </div>
    <div class="position-absolute">
      <div class="container d-flex flex-row-reverse">
        <img class="img-fluid" src="../assets/img/dc-logo-bg.png" alt="">
      </div>
    </div>
  </div>

  <div class="bottom-footer">
    <div class="container d-flex justify-content-between">
      <button type="button" class="btn btn-outline-primary">SIGN UP NOW!</button>
      <div class="right-bf d-flex align-items-center g-3">
        <h5 class="text-primary pe-4 mb-0">FOLLOW US</h5>
        <a href=""><img class="py-3 px-2" src="../assets/img/footer-facebook.png" alt=""></a>
        <a href=""><img class="py-3 px-2" src="../assets/img/footer-twitter.png" alt=""></a>
        <a href=""><img class="py-3 px-2" src="../assets/img/footer-youtube.png" alt=""></a>
        <a href=""><img class="py-3 px-2" src="../assets/img/footer-pinterest.png" alt=""></a>
        <a href=""><img class="py-3 px-2" src="../assets/img/footer-periscope.png" alt=""></a>
      </div>
    </div>
  </div>
</template>

<script>
import { footerComics } from '../data/data';
import { footerShop } from '../data/data';
import { footerDC } from '../data/data';
import { footerSites } from '../data/data';

export default {
  name: 'AppFooter',
  data() {
    return {
      buttonsComics: footerComics,
      buttonsShop: footerShop,
      buttonsDC: footerDC,
      buttonsSites: footerSites,
    }
  }
}
</script>

<style lang="scss" scoped>
.top-footer {
  width: 100%;
  height: 420px;
  background-image: url('../assets/img/footer-bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}

h3 {
  color: white;
}

a {
  color: rgb(150, 150, 150);
  text-decoration: none;
}

a:hover {
color: white;
}

.bottom-footer{
  background-color: #303030;
  padding: 40px 0px;
  }

.btn-outline-primary {
  border-radius: 0px;
  color: white;
  width: 150px;
  height: 60px;
}

.position-absolute{
  width: 100%;
  height: 420px;
  top: 0,
}

.img-fluid {
  width: 560px;
  height: 420px;
  object-fit: cover;
}

</style>