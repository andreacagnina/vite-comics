<script>
import { HeaderMenu } from '../data/Hmenu';
export default {
data(){
  return{
    HeaderMenu
  }
}

}
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="d-flex justify-content-between">
            <div class="content">
              <a href="#">
                <img src="../assets/dc-logo.png" alt="">
              </a>
            </div>
            <div class="content d-flex align-item-center">
              <ul class="d-flex my-0">
                <li
                  v-for="(label, index) in HeaderMenu"
                  :key="`HM-${index}`"><a
                  class="fw-bold"
                  :href="label.url">{{label.label}}</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/typographyColor' as *;
header {
  img {
    border: 5px solid white;
  }
}

ul {
  li {
    display: flex;
    align-items: center;
    padding: 30px 15px;
    height: 100%;
    border-top: 5px solid white;
    border-bottom: 5px solid white;

    &:hover {
      border-bottom-color: $brand_primary;
    }
    
    &:hover a {
      color: $brand_primary;
    }

    a {
      color: black;
      text-transform: uppercase;
    }
  }
}
</style>
