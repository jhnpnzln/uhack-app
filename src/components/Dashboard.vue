<template>
  <div>
    <navbar></navbar>
    <div class="mainContent">
      <!-- HEADER -->
      <div class="row">
          <div class="col-md-12">
            <h3><i class="fa fa-dashboard"></i>&nbsp;Index</h3>
          </div>
        </div>
      <!-- END HEADER -->
      
      <!-- MAP CONTAINER -->
        <div class="row row-eq-height">
          <div class="col-md-9">
            <div class="map-canvas">
              <div class="mapouter">
                <div class="gmap_canvas">
                  <iframe width="100%" height="550px" id="gmap_canvas" src="https://maps.google.com/maps?q=bacoor&t=k&z=13&ie=UTF8&iwloc=&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe>
                </div>
              </div>
            </div>
          </div>

          <div class="col-md-3">
            <div class="panel panel-green">
              <div class="panel-heading">
                <h4 class="panel-title text-center">Prone Level</h4>
              </div>
              <div class="panel-body">
                <ul class="proneLegend">
                  <li>
                    <div class="legendBullet red width"></div>
                  </li>
                  <li><router-link to="baha">Pagbaha</router-link></li>
                  <li>
                    <div class="legendBullet orange width"></div>
                  </li>
                  <li><router-link to="bagyo">Bagyo</router-link></li>
                  <li>
                    <div class="legendBullet yellow width"></div>
                  </li>
                  <li>&nbsp</li>
                  <li>
                    <div class="legendBullet green width"></div>
                  </li>
                  <li><router-link to="lindol">Lindol</router-link></li><br>
                  <li><router-link to="sunog">Sunog</router-link></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        <!-- END MAP CONTAINER -->
    </div>
  </div>
</template>
<script>
import Navbar from './Navbar'
// var marker
export default {
  components: {
    Navbar
  }
}

// Vue.components('map-content', {
//   template: '<div class="mapouter"><div class="gmap_canvas"><iframe width="819" height="852" id="gmap_canvas" src="https://maps.google.com/maps?q=bacoor&t=k&z=13&ie=UTF8&iwloc=&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe><a href="https://www.pureblack.de">pure black</a></div><style>.mapouter{overflow:hidden;height:852px;width:819px;}.gmap_canvas {background:none!important;height:852px;width:819px;}</style></div>'
// })
</script>

<style scoped>
.panel-body {
  height: 512px;
}
ul.proneLegend{
  list-style: none;
}
ul.proneLegend li {
  display: inline;
}
.legendBullet {
  height: 10px;
  width: 10px;
  padding: 5px;
  border-radius: 30px; 
}
.legendBullet.red {
  background-color: #e74c3c;
}
.legendBullet.orange {
  background-color: #e67e22;
}
.legendBullet.yellow {
  background-color: #f1c40f;
}
.legendBullet.green {
  background-color:#2ecc71;
}
#proneList {
  list-style: none;
}

/* PANEL GREEN */
.panel-green {
  border-color: #2ecc71 !important;
}
.panel-green > .panel-heading {
  background-color: #2ecc71 !important;
  color: white;
}
/* END PANEL GREEN */

/* MAP STYLE */
.map-canvas {
  width: 100%;
  height: 550px;
  border: 1px solid #000;
  border-radius: 5px;
}
.mapouter {
  overflow:hidden;
  height:550px;
  width:100%;
  }
.gmap_canvas {
  background:none!important;
  height:inherit;
  width:100%;
  }

  .width {
    width: 150px;
  }
  /* END MAP STYLE */
</style>

