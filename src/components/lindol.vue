<template>
  <div>
    <navbar></navbar>
    <div class="mainContent">
      <!-- HEADER -->
      <div class="row">
        <div class="col-md-12">
          <h3>Pag-lindol</h3>
        </div>
      </div>
      <!-- END HEADER -->

      <div class="row">
        <div class="col-md-12">
          <form-wizard color="#e67e22" title="Lindol" subtitle="Mga dapat gawin at hindi dapat gawin kapag may lindol.">
            <!-- PANEL 01 -->
            <tab-content title="Title 1" icon="fa fa-question">
              <div class="panel panel-yellow">
                <div class="panel-heading">
                  <h4 class="panel-title">Title01</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 01 -->

            <!-- PANEL 02 -->
            <tab-content title="Title 2" icon="fa fa-question">
              <div class="panel panel-warning">
                <div class="panel-heading">
                  <h4 class="panel-title">Title02</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 02 -->

            <!-- PANEL 03 -->
            <tab-content title="Title 3" icon="fa fa-question">
              <div class="panel panel-success">
                <div class="panel-heading">
                  <h4 class="panel-title">Title03</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 03 -->

            <!-- PANEL 04 -->
            <tab-content title="Title 1" icon="fa fa-question">
              <div class="panel panel-success">
                <div class="panel-heading">
                  <h4 class="panel-title">Title04</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 04 -->

            <!-- PANEL 05 -->
            <tab-content title="Title 1" icon="fa fa-question">
              <div class="panel panel-success">
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
.panel-yellow {
  border-color: #e67e22;
}
.panel-yellow > .panel-heading {
  background-color: #e67e22;
  color: white;
}
</style>

