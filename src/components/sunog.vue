<template>
  <div>
    <navbar></navbar>
    <div class="mainContent">
      <!-- HEADER -->
      <div class="row">
        <div class="col-md-12">
          <h3>Sunog</h3>
        </div>
      </div>
      <!-- END HEADER -->

      <!-- FORM WIZARD -->
      <div class="row">
        <div class="col-md-12">
          <form-wizard color="#e74c3c" title="Sunog" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may sunog."
            back-button-text="Bumalik"
            next-button-text="Sunod"
            finish-button-text="Isumite">
            <!-- PANEL 01 -->
            <tab-content title="Bago ang sunog" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title">Bago ang sunog</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 01 -->

            <!-- PANEL 02 -->
            <tab-content title="Title01" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title">Title02</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 02 -->

            <!-- PANEL 03-->
            <tab-content title="Title01" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title">Title03</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 03 -->

            <!-- PANEL 04 -->
            <tab-content title="Title01" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title">Title04</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 04 -->

            <!-- PANEL 05 -->
            <tab-content title="Title01" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title">Title05</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 05 -->
          </form-wizard>
        </div>
      </div>
      <!-- END FORM WIZARD -->
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
.panel-red {
  border-color: #e74c3c;
}
.panel-red > .panel-heading {
  background-color: #e74c3c;
  color: white;
}
</style>
