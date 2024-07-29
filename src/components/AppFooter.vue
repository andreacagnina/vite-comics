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
          <div class="col-6">
            <div class="content d-flex p-5">
              <div class="col-4">
                <div class="content">
                  <h4>
                    dc comics
                  </h4>
                  <ul class="list-unstyled my-4">
                    <li>
                      Characters
                    </li>
                    <li>
                      Comics
                    </li>
                    <li>
                      Movies
                    </li>
                    <li>
                      TV
                    </li>
                    <li>
                      Games
                    </li>
                    <li>
                      Videos
                    </li>
                    <li>
                      News
                    </li>
                  </ul>

                  <h4>
                    shop
                  </h4>
                  <ul class="list-unstyled my-4">
                    <li>Shop DC</li>
                    <li>Shop DC Collectibles</li>
                  </ul>
                </div>
              </div>
              <div class="col-4">
                <div class="content">
                  <h4>dc</h4>
                  <ul class="list-unstyled my-4">
                    <li>
                      Terms Of Use
                    </li>
                    <li>
                      Privacy policy(New)
                    </li>
                    <li>
                      Add Choices
                    </li>
                    <li>
                      Advertising
                    </li>
                    <li>
                      Jobs
                    </li>
                    <li>
                      Subscriptions
                    </li>
                    <li>
                      Talent Workshops
                    </li>
                    <li>
                      CPSC Certificates
                    </li>
                    <li>
                      Ratings
                    </li>
                    <li>
                      Shop Help
                    </li>
                    <li>
                      Contact Us
                    </li>
                  </ul>
                </div>
              </div>
              <div class="col-4">
                <div class="content">
                  <h4>sites</h4>
                  <ul class="list-unstyled my-4">
                    <li>
                      Characters
                    </li>
                    <li>
                      DC
                    </li>
                    <li>
                      MAD Magazine
                    </li>
                    <li>
                      DC Kids
                    </li>
                    <li>
                      DC Universe
                    </li>
                    <li>
                      DC Power Visa
                    </li>
                  </ul>
                </div>
              </div>
            </div>

          </div>
          <div class="col-6">
            <div class="content">
              <img src="/src/assets/dc-logo-bg.png" alt="">
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

  li {
    color: gray
  }

  a {
    text-decoration: none;
    color: black;
  }


}

.top-footer {
  background-image: url(/src/assets/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  height: 500px;

}

.bottom-footer {
  background-color: #303030;
  position: relative;
  z-index: 1;

  li {
    padding: 20px 15px;
  }
}
</style>
