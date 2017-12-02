<template>
  <div>
    <nav class="navbar navbar-light bg-faded navbar-fixed-top">
      <div class="logo-container">
        <router-link :to="{path: '/'}" class="navbar-brand" style="color: white;">
          <img src="statics/flat-pinoy-icon.png" width="50" height="50" class="d-inline-block align-top logo" alt="">
        </router-link>
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
  position: fixed;
  z-index: 1;
  top: 0;
  left: 10px;
}
.logo-container a {
  position: static;
}
</style>

