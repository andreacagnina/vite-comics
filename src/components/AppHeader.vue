<script>
export default {
data(){
  return{
    links: [
      {
      label: 'characters',
      url: '#',
    },
      {
      label: 'comics',
      url: '#',
    },
      {
      label: 'movie',
      url: '#',
    },
      {
      label: 'tv',
      url: '#',
    },
      {
      label: 'games',
      url: '#',
    },
      {
      label: 'collectibles',
      url: '#',
    },
      {
      label: 'videos',
      url: '#',
    },
      {
      label: 'fans',
      url: '#',
    },
      {
      label: 'news',
      url: '#',
    },
      {
      label: 'shop',
      url: '#',
    },
    ]
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
              <ul class="list-unstyled d-flex my-0">
                <li v-for="(label, index) in links" :key="index"><a class="fw-bold" :href="label.url">{{label.label}}</a></li>

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
  background-color: white;

  img {
    border: 5px solid white;
  }
}

ul {
  li {
    padding: 30px 15px;
    height: 100%;
    display: flex;
    align-items: center;
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
      text-decoration: none;
      text-transform: uppercase;


    }
  }
}
</style>
