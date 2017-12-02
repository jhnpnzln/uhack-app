<template>
  <div>
    <navbar></navbar>
    <div class="mainContent lindolBody">
      <!-- HEADER -->
      <div class="row">
        <div class="col-md-12">
          <h3>Pag-lindol</h3>
        </div>
      </div>
      <!-- END HEADER -->

      <div class="row">
        <div class="col-md-12">
          <form-wizard @on-complete="onCompleteLindol" color="#e67e22" title="Lindol" subtitle="Mga dapat gawin bago, habang at pagkatapos ng lindol."
            back-button-text="Bumalik"
            next-button-text="Sunod"
            finish-button-text="Isumite">
            <!-- PANEL 01 -->
            <tab-content title="Bago lumindol" icon="fa fa-question">
              <div class="panel panel-yellow">
                <div class="panel-heading">
                  <h4 class="panel-title">Bago lumindol</h4>
                </div>
                <div class="panel-body">
                  <p>- Patayin ang kuryente, tubig, at gas.</p>
                  <p>- Ihanda ang fire extinguisher, flashlights, battery-powered radio, ekstrang batteries, at first aid kit sa bahay.</p>
                  <p>- Magkakaroon ng plano kung saan magtatagpo ang miyembro ng pamilya habang o pagkatapos ng lindol.</p>
                  <p>- Alamin ang earthquake plan sa bahay, opisina o paaralan. Mabuting sumali rin sa earthquake drill.</p>
                </div>
              </div>
            </tab-content>
            <!-- END PANEL 01 -->

            <!-- PANEL 02 -->
            <tab-content title="Habang lumilindol" icon="fa fa-question">
              <div class="panel panel-yellow">
                <div class="panel-heading">
                  <h4 class="panel-title">Habang lumilindol</h4>
                </div>
                <div class="panel-body">
                  <p>- Kalma lang. Kung nasa loob, manatiling nasa loob. Kung nasa labas, manatiling nasa labas.</p>
                  <p>- Gumapang papunta sa ilalim ng matitibay o mabibigat na muebles o lamesa.</p>
                  <p>- Kapag nasa sasakyan, siguraduhing malayo sa mataas na gusali at manatili lamang sa loob ng sasakyan.</p>
                  <p>- Kung nasa loob, iwasang dumikit o lumapit sa mga salamin o mahihinang pundasyon ng gusali.</p>
                </div>
              </div>
            </tab-content>
            <!-- END PANEL 02 -->

            <!-- PANEL 03 -->
            <tab-content title="Pagkatapos lumindol" icon="fa fa-question">
              <div class="panel panel-yellow">
                <div class="panel-heading">
                  <h4 class="panel-title">Pagkatapos lumindol</h4>
                </div>
                <div class="panel-body">
                  <p>- Umiwas sa may lamat nang salamin o may sirang pader dala ng lindol.</p>
                  <p>- Itsek ang linya ng tubig, gas, at kuryente at agad itong ipaayos.</p>
                  <p>- Umiwas malapit sa dagat. Posibleng magkaroon ng tsunami matapos ng malakas na lindol.</p>
                  <p>- Maghanda sa maaaring aftershocks.</p>
                </div>
              </div>
            </tab-content>
            <!-- END PANEL 03 -->
          </form-wizard>
        </div>
      </div>

    </div>

    <!-- ********* MODAL ******* -->
    <modal name="lindolModal" width="50%" height="auto" :scrollable="true">
      <div class="modal-content">
        <div class="modal-header">
          <button type="button" class="close" @click="closeModal" style="color:white;">&times;</button>
          <h4 class="modal-title"><i class="fa fa-question-circle"></i>&nbsp;Mga Tanong</h4>
        </div>
      </div>
      <div class="modal_body">
        <form action="">
          <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>1. Magwalang bahala, matatapos din yan..  </p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio1"/>
                      <label for="radio1">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio2" />
                      <label for="radio2">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

            <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>2. Iiwasan natin ang malapit sa dagat ?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio3"/>
                      <label for="radio3">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio3" />
                      <label for="radio3">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>3. Alamin ang earthquake plan sa bahay, opisina o paaralan.</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio4"/>
                      <label for="radio4">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio5" />
                      <label for="radio5">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>4. Magtago sa ilalim ng lamesa. </p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio6"/>
                      <label for="radio6">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio7" />
                      <label for="radio7">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>5. Ihahanda ba natin ang ating sarili dulot ng lindol?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio8"/>
                      <label for="radio8">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio9" />
                      <label for="radio9">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>6. Patayin ang kuryente, tubig, at gas kapag nagbigay ng babala ang lokal na pamahalaan?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio10"/>
                      <label for="radio8">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio11" />
                      <label for="radio9">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="button-cotainer pull-right">
                <button class="btn btn-success" @click="submit"><i class="fa fa-check"></i>&nbsp;Isumite</button>
                <button class="btn btn-default"><i class="fa fa-ban"></i>&nbsp;Ikansela</button>
              </div>

        </form>
      </div>
    </modal>
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
  },
  methods: {
    onCompleteLindol () {
      this.$modal.show('lindolModal')
    },
    closeModal () {
      this.$modal.hide('lindolModal')
    },
    submit () {
      this.closeModal()
      this.$toastr.success('Na-isumite na.', 'Ayos!')
    }
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
.lindolBody {
  background-image: url('/statics/lindol-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  height: 650px;
  overflow: hidden;
}
.modal-header {
  background-color: #e67e22;
  color: white;
}
</style>
