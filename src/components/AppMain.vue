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
      ],
      comics:[
  {
    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
    price: "$19.99",
    series: "Action Comics",
    type: "comic book"
  },
  {
    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
    price: "$3.99",
    series: "American Vampire 1976",
    type: "comic book"
  },
  {
    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
    price: "$16.99",
    series: "Aquaman",
    type: "graphic novel"
  },
  {
    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
    price: "$2.99",
    series: "Batgirl",
    type: "comic book"
  },
  {
    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
    price: "$3.99",
    series: "Batman",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg/revision/latest?cb=20080809201655",
    price: "$2.99",
    series: "Batman Beyond",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg/revision/latest/scale-to-width-down/1200?cb=20130627211607",
    price: "$3.99",
    series: "Batman/Superman",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg/revision/latest?cb=20200929145132",
    price: "$4.99",
    series: "Batman/Superman Annual",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg/revision/latest?cb=20200929124651",
    price: "$5.99",
    series: "Batman: The Joker War Zone",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg/revision/latest?cb=20201123054610",
    price: "$6.99",
    series: "Batman: Three Jokers",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg/revision/latest?cb=20201124094800",
    price: "$4.99",
    series: "Batman: White Knight Presents: Harley Quinn",
    type: "comic book"
  },
  {
    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg/revision/latest?cb=20160303223223",
    price: "$16.99",
    series: "Catwoman",
    type: "graphic novel"
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
          <div class="col-12">
            <div class="row">
              <div v-for="(comic, index) in comics" :key="index" class="col-2 content my-3">
                <img :src="comic.thumb" :alt="comic.series" class="w-100">
                <h6>{{comic.series}}</h6>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
        <section>
          <div class="container section-two">
            <div class="row">
              <div class="col-12">
                  <div class="content justify-content-between px-5">
                    <ul class="d-flex  align-items-center my-0 justify-content-around text-center text-nowrap">
                    <li
                        class="d-flex"
                        v-for="(icon, index) in icons"
                        :key="index"><a
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


    &:nth-child(2) {
      background-color: $brand_primary;
    }

  }
  
  .section-two{
    a {
      text-transform: uppercase;
    }
  
    li:nth-child(4){
      width: 15%;
    }
  
    li:last-child {
      width: 25%;
    }
    img {
      width: 20%;
      margin-right: 10px;
    }
  }
  img {
    aspect-ratio: 1/1;
  }
  }
</style>
