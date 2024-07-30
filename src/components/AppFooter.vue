<script>
import { faIcons, DcComics, shop, Dc, sites } from '../data/Fmenu';

export default {
  data(){
    return{
      faIcons,
      DcComics,
      shop,
      Dc,
      sites
      
    }
  }

}
</script>

<template>
  <footer>

    <div class="top-footer">
      <div class="container">
        <div class="row">
          <div class="col-12 ">
            <div class="content d-flex py-5 bg-image-logo">
              <div class="col-2">
                <div class="content">
                  <h4>
                    dc comics
                  </h4>
                  <ul class="my-3">
                    <li
                    v-for="(label, index) in DcComics"
                    :key="`DcC-${index}`"><a
                    :href="label.url">
                    {{label.label}}</a>
                    </li>
                  </ul>

                  <h4>
                    shop
                  </h4>
                  <ul class="my-3">
                    <li
                      v-for="(label, index) in shop"
                      :key="`shop-${index}`"><a
                      :href="label.url">{{label.label}}</a></li>
                  </ul>
                </div>
              </div>
              <div class="col-2">
                <div class="content">
                  <h4>dc</h4>
                  <ul class="my-3">
                    <li
                      v-for="(label, index) in Dc"
                      :key="`dc-${index}`"><a
                      :href="label.url">{{label.label}}</a></li>
                  </ul>
                </div>
              </div>
              <div class="col-2">
                <div class="content">
                  <h4>sites</h4>
                  <ul class="my-3">
                    <li
                      v-for="(label, index) in sites"
                      :key="`sites-${index}`"><a
                      :href="label.url">{{label.label}}</a></li>
                  </ul>
                </div>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>

    <div class="bottom-footer">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="d-flex justify-content-between align-items-center">
              <div class="content">
                <button type="button" class="butn">SIGN-UP-NOW!</button>
              </div>

              <div class="content d-flex align-item-center">
                <ul class="d-flex align-items-center my-0">
                  <li><a class="fw-bold" href="">FOLLOW US</a></li>
                  <li
                    v-for="(icon, index) in faIcons"
                    :key="`FaFo-${index}`"><a
                    href=""><img
                    :src="icon.url"
                    alt=""></a></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/typographyColor' as *;
footer {
  h4 {
    text-transform: uppercase;
  }

  a {
    color: gray;
    
    &:hover {
      color: white
    }
  }
}

.bg-image-logo {
  background-image: url(/src/assets/dc-logo-bg.png);
  background-repeat: no-repeat;
  background-position: right;

}

.top-footer {
  background-image: url(/src/assets/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;

}

.bottom-footer {
  background-color: #303030;


  li {
    padding: 20px 15px;

    a:first-child {
      color: $brand_primary
    }
    img:hover {
      background-color: $brand_primary;
      border-radius: 50%;
    }
  }
}

.butn {
  border: 1px solid $brand_primary;
  color: white;
  padding: 7px 10px;
  background-color: #303030;

  &:hover {
    background-color: $brand_primary;
  }
}
</style>
