<script>
export default {

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
                <li><a class="fw-bold" href="">characters</a></li>
                <li><a class="fw-bold" href="">comics</a></li>
                <li><a class="fw-bold" href="">movies</a></li>
                <li><a class="fw-bold" href="">tv</a></li>
                <li><a class="fw-bold" href="">games</a></li>
                <li><a class="fw-bold" href="">collectibles</a></li>
                <li><a class="fw-bold" href="">videos</a></li>
                <li><a class="fw-bold" href="">fans</a></li>
                <li><a class="fw-bold" href="">news</a></li>
                <li><a class="fw-bold" href="">shop</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  background-color: white;


  img {
    border-bottom: 5px solid white;
  }
}

ul {
  li {
    padding: 30px 15px;
    height: 100%;
    display: flex;
    align-items: center;
    border-bottom: 5px solid white;

    &:hover {
      border-bottom: 5px solid #0c7cec;
    }

    a {
      text-decoration: none;
      color: #0c7cec;
      text-transform: uppercase;


    }
  }
}
</style>
