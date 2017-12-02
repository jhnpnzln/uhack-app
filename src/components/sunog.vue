<template>
  <div>
    <navbar></navbar>
    <div class="mainContent sunogBody">
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
          <form-wizard  @on-complete="onCompleteSunog" color="#e74c3c" title="Sunog" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may sunog."
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
                    <p> 1. Alamin ang fire exit. </p>
                    <p> 2. Magkaroon ng pagsasanay sa ginawang plano, dalawang beses sa isang taon. </p>
                    <p> 3. Tiyakin na alam ng bawat miyembro ng pamilya kung paano magbukas ng nakakandado o hinarangang pinto at bintana. </p>
                     <p>4. Ang mga nakakadadong pinto at bintana ay dapat madaling mabuksan sa panahon ng kagipitan. </p>
                </div>
              </div>
            </tab-content>
            <!-- END PANEL 01 -->

            <!-- PANEL 02 -->
            <tab-content title="Habang nasaloob ng sunog" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title"></h4>
                </div>
                <div class="panel-body">
                    <p>1. Huwag magpanic, maging alisto at mahinahon. </p>
                    <p> 2. Patayin ang main switch ng kuryente bago patayin ang apoy. </p>
                    <p> 3. Subukang patayin ang apoy habang maliit pa.  </p>
                    <p> 4. Tumawag ng bumbero. </p>
                </div>
              </div>                    
            </tab-content>
            <!-- END PANEL 02 -->

            <!-- PANEL 03-->
            <tab-content title="Pagkatapos ng sunog" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title"></h4>
                </div>
                <div class="panel-body">
                  <p> 1. Iwasang lumapit sa lugar kung saan naganap ang sunog. </p>
                   <p>2. Tiyakin na nainspeksyon ng mga kinauukulan ang inyong bahay </p>
                   <p>3. Alisin ang mga bagay na maaaring magdulot ng karagdagang pinsala. </p>

                </div>
              </div>
            </tab-content>
            <!-- END PANEL 03 -->
            <!-- END PANEL 05 -->
          </form-wizard>
        </div>
      </div>
      <!-- END FORM WIZARD -->
    </div>

    <!-- ********** MODAL *********** -->
    <modal name="sunogModal" width="50%" height="auto" :scrollable="true">
      <div class="modal-content">
        <div class="modal-header">
          <button type="button" class="close" @click="closeModal" style="color:white;">&times;</button>
          <h4 class="modal-title"><i class="fa fa-question-circle"></i>&nbsp;Mga Tanong</h4>
        </div>
      </div>

      <div class="modal_body">
        <form action="">
          <div class="form-group row">
            <div class="funkyradio">
                <div class="col-md-12 col-xs-6">
                  <p>1.Nainspekyun na ng kinauukulan ang iyong bahay?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" value="Tama"  v-model="slctQ1" name="radio1" id="radio1" />
                      <label for="radio1">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio"  value="Mali"  v-model="slctQ1"  name="radio1" id="radio2"  />
                      <label for="radio2">Mali</label>
                    </div>
                  </div>
                </div>
            </div>
          </div>

          <div class="form-group row">
            <div class="funkyradio">
                <div class="col-md-12 col-xs-6">
                  <p>2.Tumawag ng bumbero. </p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" value="Tama" v-model="slctQ2" name="radio2" id="radio3" />
                      <label for="radio3">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" value="Mali" v-model="slctQ2" name="radio2" id="radio4" />
                      <label for="radio4">Mali</label>
                    </div>
                  </div>
                </div>
            </div>
          </div>

          <div class="form-group row">
            <div class="funkyradio">
                <div class="col-md-12 col-xs-6">
                  <p>3.Aalisin ba natin ang mga bagay na pedeng mag bigay ng karagdagang sunog?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" value="Tama" v-model="slctQ3" name="radio3" id="radio5"/>
                      <label for="radio5">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" value="Mali" v-model="slctQ3" name="radio3" id="radio6"  />
                      <label for="radio6">Mali</label>
                    </div>
                  </div>
                </div>
            </div>
          </div>

          <div class="form-group row">
            <div class="funkyradio">
                <div class="col-md-12 col-xs-6">
                  <h4 class="panel-title">4.Ibaba ang main switch?</h4>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-warning">
                      <input type="radio" value="Tama" v-model="slctQ4" name="radio4" id="radio7" />
                      <label for="radio7">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" value="Mali" v-model="slctQ4" name="radio4" id="radio8"  />
                      <label for="radio8">Mali</label>
                    </div>
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
  data: function () {
    return {
      slctQ1: '',
      slctQ2: '',
      slctQ3: '',
      slctQ4: '',
      score: 0,
      pass: 2
    }
  },
  components: {
    Navbar,
    FormWizard,
    TabContent
  },
  methods: {
    onCompleteSunog () {
      this.$modal.show('sunogModal')
    },
    closeModal () {
      this.$modal.hide('sunogModal')
    },
    submit () {
      if (this.slctQ1 === 'Tama') {
        this.score++
      }
      if (this.slctQ2 === 'Tama') {
        this.score++
      }
      if (this.slctQ3 === 'Tama') {
        this.score++
      }
      if (this.slctQ4 === 'Tama') {
        this.score++
      }
      if (this.score > this.pass) {
        this.$toastr.success('Nakakuha ka ng mataas na puntos', 'Puntos')
        this.$toastr.success('Naipasamo ang pagsusulit.', 'Ayos!')
        this.closeModal()
        this.$router.push('/')
      }
      else {
        this.$toastr.success('Ang nakuha mong puntos ay mababa', 'Puntos')
        this.$modal.hide('sunogModal')
      }
    }
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
.sunogBody {
  background-image: url('/statics/sunog-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  height: 650px;
  overflow: hidden;
}
.modal-header {
  background-color: #e74c3c;
  color: white;
}
</style>
