<script>
import { icons } from '../data/Mmenu';
import { comicsCard } from '../data/cardMmenu';
import CardComics from './CardComics.vue';
import Jumbotron from './Jumbotron.vue';



export default {
  components:{
    CardComics,
    Jumbotron
  },
  data(){
    return{
  icons,
  comicsCard,
    }
}
}
</script>

<template>
  <main>
<div class="jumbotron">
  <Jumbotron/>
  <Button class="button abs">CURRENT SERIES</Button>
</div>
    <section>
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="row">
              <CardComics v-for="(comic, index) in comicsCard" :key="`CardComics-${index}`" :Card="comic"/>
            </div>
          </div>
          <div class="col-12">
            <div class="content text-center">
              <button class="button">Load more</button>
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
  .jumbotron {
    position: relative;

    .abs {
      position: absolute;
      bottom: -17px;
      left: 15%;
          }
        }
        
        .button {
          background-color: $brand_primary;
          color: white;
          border: none;
          padding: 5px 25px;
          text-transform: uppercase;
        }
  section {
    background-color: black;
    padding: 20px;

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
