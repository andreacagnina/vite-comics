<script>
export default {
  data(){
    return{
      icons: [
        {
          label: 'digital comics',
          url: '/src/assets/buy-comics-digital-comics.png',
        },
        {
          label: 'dc merchandise',
          url: '/src/assets/buy-comics-merchandise.png',
        },
        {
          label: 'subscription',
          url: '/src/assets/buy-comics-subscriptions.png',
        },
        {
          label: 'comic shop locator',
          url: '/src/assets/buy-comics-shop-locator.png',
        },
        {
          label: 'dc power visa',
          url: '/src/assets/buy-dc-power-visa.svg',
        }
      ]
    }
}
}
</script>

<template>
  <main>
    <section>
      <div class="container">
        <div class="row">
          <div class="col-12"><div class="content"> -->Content goes here<-- </div></div>
        </div>
      </div>
    </section>
        <section>
          <div class="container">
            <div class="row">
              <div class="col-12">
                  <div class="content justify-content-between px-5">
                    <ul class="list-unstyled d-flex  align-items-center my-0 justify-content-around text-center text-nowrap">
                      <li class="d-flex" v-for="(icon, index) in icons" :key="index"><a href=""><img :src="icon.url" alt="">{{icon.label}}</a></li>
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
    color: white;

    &:nth-child(2) {
      background-color: $brand_primary;
    }

    a {
      color: white;
      text-decoration: none;
      text-transform: uppercase;
    }

    li:nth-child(4){
      width: 15%;
    }

    li:last-child {
      width: 25%;
    }
  }

  img {
    width: 20%;
    margin-right: 10px
  };




}
</style>
