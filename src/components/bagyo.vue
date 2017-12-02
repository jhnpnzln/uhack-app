<template>
  <div>
    <navbar></navbar>
    <div class="mainContent bagyoBody">
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
          <form-wizard @on-complete="onCompleteBagyo" color="#1abc9c" title="Bagyo" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may bagyo."
            back-button-text="Bumalik"
            next-button-text="Sunod"
            finish-button-text="Isumite">
    
            <!-- PANEL 01 -->
            <tab-content title="Bago bumagyo" icon="fa fa-info">
              <div class="panel panel-turquoise">
              <div class="panel-heading">
                <h4 class="panel-title">
                 
                </h4>
              </div>
              <div class="panel-body">
                  <p>1. Iakyat ang gamit sa mas mataas na lugar.</p>
<p>2. Kapag inutos ang paglikas, sumunod kaagad. Huwag mag-panic. Pumunta sa evacuation area bago pa man bahain ang daanan patungo rito.</p>
<p>3. Magtabi ng malinis na inuming tubig sa mga sisidlan dahil posibleng maputol ang serbisyo ng patubig.</p>
<p>4. Patayin ang main switch ng kuryente at tangke ng gas.</p>

              </div>
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
              <div class="panel-body">


                <p>1. Manatili sa loob ng bahay o evacuation area.</p>
                   <p> 2. Huwag lalangoy o mamangka sa mga ilog na umaapaw.</p>
                   <p> 3. Lumayo sa mga bumagsak na poste at iba pang mataas na bagay.</p>
                   <p> 4. Maging alerto sa gas leaks. Gamitin ang flashlight sa pag-iinspekto nito.</p>
              </div>
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
              <div class="panel-body">
                   <p>1. I-report ang putol na kawad/kable/tubo (kuryente, tubig, gas at telepono) sa kinauukulan.</p>
                    <p>2. Bantayan ang mga bagay na pwedeng pagmulan ng sunog gaya ng mga putol na kawad ng kuryente.</p>
                    <p>3. Huwag sindihan ang main switch o gumamit ng appliances na hindi pa nasusuri ng electrician.</p>
                    <p>4. Huwag mamasyal o maki-usyoso sa lugar na tinamaan ng sakuna upang di makasagabal sa rescue at iba pang emergency operations.</p>
               </div>
            </div>
            </tab-content>
            <!-- END PANEL 02 -->
          </form-wizard>
        </div>
      </div>
      <!-- END WIZARD FORM -->
    </div>

    <!-- ************** MODAL *************** -->
    <modal name="bagyoModal" width="50%" height="auto" :scrollable="true">
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
                  <p>1. Makinig sa radyo o manood sa telebisyon tungkol sa weather updates</p>
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
                  <p>2. Natiyak ba nating ang kable o outlet ay sakaling nakababad sa tubig?</p>
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
                      <input type="radio" name="radio" id="radio4" />
                      <label for="radio4">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>3. Nasuri mo ang iyong bahay kung ito ba ay matibay ,Manatili sa loob ng bahay? </p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio5"/>
                      <label for="radio5">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio6" />
                      <label for="radio6">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>4. Mangisda sa kasagsagan ng bagyo?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio7"/>
                      <label for="radio7">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio8" />
                      <label for="radio8">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>5. Maghanda ng ilawan at radyong de baterya</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" name="radio" id="radio9"/>
                      <label for="radio9">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio10" />
                      <label for="radio10">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="button-container pull-right">
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
    onCompleteBagyo () {
      this.$modal.show('bagyoModal')
    },
    closeModal () {
      this.$modal.hide('bagyoModal')
    },
    submit () {
      this.$toastr.success('Naisumite na.', 'Ayos!')
      this.closeModal()
    }
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
.bagyoBody {
  background-image: url('/statics/bagyo-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  height: 650px;
  overflow: hidden;
}
.modal-header {
  background-color: #1abc9c;
  color: white;
}
</style>


