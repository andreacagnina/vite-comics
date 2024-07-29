<script>
export default {

}
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-2">
        </div>
        <div class="col-12">
          <div class="d-flex justify-content-between align-items-stretch">
            <div class="content bg-warning">
              <a href="#">
                <img src="../assets/dc-logo.png" alt="">
              </a>
            </div>

            <div class="content bg-danger d-flex align-item-center">
              <ul class="list-unstyled d-flex my-0">
                <li><a href="">1</a></li>
                <li><a href="">2</a></li>
                <li><a href="">3</a></li>
                <li><a href="">4</a></li>
                <li><a href="">5</a></li>
                <li><a href="">6</a></li>
                <li><a href="">7</a></li>
                <li><a href="">8</a></li>
                <li><a href="">9</a></li>
                <li><a href="">10</a></li>
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
  padding: 20px 20px 0 20px;
}

ul {
  li {
    padding: 30px;
    border: 5px solid lightblue;



    a {
      text-decoration: none;
      color: black;
    }
  }
}
</style>
