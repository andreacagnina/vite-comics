<script>
export default {
  data(){
    return{
      icons: [
        {
          url: '/src/assets/buy-comics-digital-comics.png',
        },
        {
          url: '/src/assets/buy-comics-merchandise.png',
        },
        {
          url: '/src/assets/buy-comics-subscriptions.png',
        },
        {
          url: '/src/assets/buy-comics-shop-locator.png',
        },
        {
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
      -->Content goes here<-- </section>
        <section>
          <div class="container">
            <div class="row">
              <div class="col-12">
                  <div class="content justify-content-between px-5">
                    <ul class="list-unstyled d-flex  align-items-center my-0 justify-content-around text-center">
                      <li v-for="(icon, index) in icons" :key="index"><a href=""><img :src="icon.url" alt=""></a></li>
                    </ul>
                  </div>
              </div>
            </div>
          </div>
        </section>
  </main>
</template>

<style lang="scss" scoped>
main {
  section {
    background-color: black;
    padding: 50px;
    color: white;

    &:nth-child(2) {
      background-color: #0282f9;
      position: relative;
      z-index: 1;
    }
  }

  img {
    width: 40%;
  };


}
</style>
