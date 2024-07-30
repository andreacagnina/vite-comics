<script>
import { icons } from '../data/Mmenu';
import { comicsCard } from '../data/cardMmenu';
import CardComics from './CardComics.vue';


export default {
  components:{
    CardComics,
  },
  data(){
    return{
  icons,
  comicsCard
    }
}
}
</script>

<template>
  <main>
    <section>
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="row">
              <CardComics v-for="(comic, index) in comicsCard" :key="`CardComics-${index}`" :Card="comic"/>
            </div>
          </div>
        </div>
      </div>
    </section>
        <section class="section-two">
          <div class="container">
            <div class="row">
              <div class="col-12">
                  <div class="content justify-content-between px-5">
                    <ul class="d-flex  align-items-center my-0 justify-content-around text-center text-nowrap">
                    <li
                        class="d-flex"
                        v-for="(icon, index) in icons"
                        :key="`icon-${index}`"><a
                        href=""><img
                        :src="icon.url"
                        alt="">{{icon.label}}</a></li>
                    </ul>
                  </div>
              </div>
            </div>
          </div>
        </section>
  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/typographyColor' as *;
main {
  section {
    background-color: black;
    padding: 60px;


  }
  .section-two{
    background-color: $brand_primary;

    a {
      text-transform: uppercase;
    }
  
    img {
      width: 40px;
      margin-right: 10px;
    }

    li:nth-child(4){
      img {
        width: 25px;
      }
    }
  }

  }
</style>
