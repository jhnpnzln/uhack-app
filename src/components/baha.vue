<template>
  <div>
    <navbar></navbar>
    <div class="mainContent">
      <div class="row">
        <div class="col-md-12">
          <h3>Pag-baha</h3>
        </div>
      </div>

      <div class="row">
        <div class="col-md-12">
          <form-wizard color="#337ab7" title="Baha" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may pag-baha.">
            <!-- QUESTION 1 -->
            <tab-content title="Title 1" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Title01</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 1 -->

            <!-- QUESTION 2 -->
            <tab-content title="Title 2" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Title02</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 2 -->

            <!-- QUESTION 3 -->
            <tab-content title="Title 3" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Title03</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 3 -->

            <!-- QUESTION 4 -->
            <tab-content title="Title 4" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Title04</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 4 -->

            <!-- QUESTION 4 -->
            <tab-content title="Title 5" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Title05</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 5 -->

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
