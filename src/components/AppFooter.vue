<script>
export default {
  data(){
    return{
      faIcons: [
        {
          url: '/src/assets/footer-facebook.png',
        },
        {
          url: '/src/assets/footer-twitter.png',
        },
        {
          url: '/src/assets/footer-youtube.png',
        },
        {
          url: '/src/assets/footer-pinterest.png',
        },
        {
          url: '/src/assets/footer-periscope.png',
        },
      ],

      DcComics: [
        {
          label: 'Characters',
          url: '',
          current: false,
        },
        {
          label: 'Comics',
          url: '',
          current: false,
        },
        {
          label: 'Movies',
          url: '',
          current: false,
        },
        {
          label: 'TV',
          url: '',
          current: false,
        },
        {
          label: 'Games',
          url: '',
          current: false,
        },
        {
          label: 'Videos',
          url: '',
          current: false,
        },
        {
          label: 'News',
          url: '',
          current: false,
        },

      ],
      shop: [
        {
          label: 'Shop DC',
          url: '',
          current: false,
        },
        {
          label: 'Shop DC Collectibles',
          url: '',
          current: false,
        },
      ],
      Dc: [
        {
          label: 'Terms Of Use',
          url: '',
          current: false,
        },
        {
          label: 'Privacy policy(New)',
          url: '',
          current: false,
        },
        {
          label: 'Add Choices',
          url: '',
          current: false,
        },
        {
          label: 'Advertising',
          url: '',
          current: false,
        },
        {
          label: 'Jobs',
          url: '',
          current: false,
        },
        {
          label: 'Subscriptions',
          url: '',
          current: false,
        },
        {
          label: 'Talent Workshops',
          url: '',
          current: false,
        },
        {
          label: 'CPSC Certificates',
          url: '',
          current: false,
        },
        {
          label: 'Ratings',
          url: '',
          current: false,
        },
        {
          label: 'Shop Help',
          url: '',
          current: false,
        },
        {
          label: 'Contact Us',
          url: '',
          current: false,
        },
        
      ],
      sites:[
        {
          label: 'Characters',
          url: '',
          current: false,
        },
        {
          label: 'DC',
          url: '',
          current: false,
        },
        {
          label: 'MAD Magazine',
          url: '',
          current: false,
        },
        {
          label: 'DC Kids',
          url: '',
          current: false,
        },
        {
          label: 'DC Universe',
          url: '',
          current: false,
        },
        {
          label: 'DC Power Visa',
          url: '',
          current: false,
        },
      ]

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
                  <ul class="list-unstyled my-3">
                    <li v-for="(label, index) in DcComics" :key="index"><a :href="label.url"> {{label.label}}</a>
                    </li>
                  </ul>

                  <h4>
                    shop
                  </h4>
                  <ul class="list-unstyled my-3">
                    <li v-for="(label, index) in shop" :key="index"><a :href="label.url">{{label.label}}</a></li>
                
                  </ul>
                </div>
              </div>
              <div class="col-2">
                <div class="content">
                  <h4>dc</h4>
                  <ul class="list-unstyled my-3">
                    <li v-for="(label, index) in Dc" :key="index"><a :href="label.url">{{label.label}}</a></li>
                  </ul>
                </div>
              </div>
              <div class="col-2">
                <div class="content">
                  <h4>sites</h4>
                  <ul class="list-unstyled my-3">
                    <li v-for="(label, index) in sites" :key="index"><a :href="label.url">{{label.label}}</a></li>
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
                <button type="button" class="btn btn-outline-primary">SIGN-UP-NOW!</button>
              </div>

              <div class="content d-flex align-item-center">
                <ul class="list-unstyled d-flex align-items-center my-0">
                  <li><a class="text-primary fw-bold" href="">FOLLOW US</a></li>
                  <li v-for="(icon, index) in faIcons" :key="index"><a href=""><img :src="icon.url" alt=""></a></li>
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
footer {
  color: white;

  h4 {
    text-transform: uppercase;
  }

  a {
    text-decoration: none;
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
  }
}
</style>
