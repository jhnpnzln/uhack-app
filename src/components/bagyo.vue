<template>
  <div>
    <navbar></navbar>
    <div class="mainContent">
      <!-- HEADER -->
        <div class="row">
          <div class="col-md-12">
            <h3>Bagyo</h3>
          </div>
        </div>
      <!-- END HEADER -->

      <!-- WIZARD FORM -->
      <div class="row">
        <div class="col-md-12">
          <form-wizard color="#1abc9c" title="Baha" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may bagyo."
            back-button-text="Bumalik"
            next-button-text="Sunod"
            finish-button-text="Isumite">
    
            <!-- PANEL 01 -->
            <tab-content title="Bago bumagyo" icon="fa fa-info">
              <div class="panel panel-turquoise">
              <div class="panel-heading">
                <h4 class="panel-title">
                  Bago bumagyo
                </h4>
              </div>
              <div class="panel-body"></div>
            </div>
            </tab-content>
            <!-- END PANEL 01 -->

            <!-- PANEL 02 -->
            <tab-content title="Habang bumabagyo" icon="fa fa-info">
              <div class="panel panel-turquoise">
              <div class="panel-heading">
                <h4 class="panel-title">
                  Habang bumabagyo
                </h4>
              </div>
              <div class="panel-body"></div>
            </div>
            </tab-content>
            <!-- END PANEL 02 -->

            <!-- PANEL 02 -->
            <tab-content title="Pagkatapos ng bagyo" icon="fa fa-info">
              <div class="panel panel-turquoise">
              <div class="panel-heading">
                <h4 class="panel-title">
                  Pagkatapos ng bagyo
                </h4>
              </div>
              <div class="panel-body"></div>
            </div>
            </tab-content>
            <!-- END PANEL 02 -->
          </form-wizard>
        </div>
      </div>
      <!-- END WIZARD FORM -->
    </div>
  </div>
</template>

<script>
import Navbar from './Navbar'
import {FormWizard, TabContent} from 'vue-form-wizard'
export default {
  components: {
    Navbar,
    FormWizard,
    TabContent
  }
}
</script>
<style scoped>
.panel-turquoise {
  border-color: #1abc9c;
}
.panel-turquoise > .panel-heading {
  background-color: #1abc9c;
  color: white;
}
</style>


