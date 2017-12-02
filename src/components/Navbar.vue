<template>
  <div>
    <nav class="navbar navbar-light bg-faded">
      <div class="logo-container">
        <router-link :to="{path: '/'}" class="navbar-brand" style="color: white;">
          <img src="statics/flat-pinoy-icon.png" width="50" height="50" class="d-inline-block align-top logo" alt="">
        </router-link>     
      </div>
      <div class="pull-right" style="padding-right:50px">
        0
        <img src="http://www.myrestaurantappbuilder.com/wp-content/uploads/2015/07/lesson_coupon.png" width="50" height="35" class="d-inline-block align-top logo" alt="">
      </div>
    </nav>

    <aside>

    </aside>
  </div>
</template>

<style scoped>
.navbar{
  border-radius: 0 !important;
  background-color: #2ecc71 !important;
  margin-bottom: 0 !important;
}
.logo-container {
  z-index: 1;
  top: 0;
  left: 10px;
}
.logo-container a {
  position: static;
}
</style>

