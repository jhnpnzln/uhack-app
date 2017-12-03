<template>
  <div>
    <navbar></navbar>
    <div class="mainContent bahaBody">
      <div class="row">
        <div class="col-md-12">
          <h3>Pag-baha</h3>
        </div>
      </div>

      <div class="row">
        <div class="col-md-12">
          <form-wizard @on-complete="onCompleteBaha" color="#337ab7" title="Baha" subtitle="Mga bagay na dapat gawin bago, habang at pagkatapos ng pagbaha."
            back-button-text="Bumalik"
            next-button-text="Sunod"
            finish-button-text="Isumite">
            <!-- QUESTION 1 -->
            <tab-content title="Bago ang pag-baha" icon="fa fa-info">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Bago ang pag-baha</h4>
                </div>
                <div class="panel-body">
                  <p>- Iakyat ang gamit sa mas mataas na lugar.</p>
                  <p>- Kapag inutos ang paglikas, sumunod kaagad. Huwag mag-panic. 
                  Pumunta sa evacuation area bago pa man bahain ang daanan patungo rito.</p>
                  <p>- Magtabi ng malinis na inuming tubig sa mga sisidlan dahil posibleng maputol ang serbisyo ng patubig.</p>
                  <p>- Patayin ang main switch ng kuryente at tangke ng gas.</p>
                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 1 -->

            <!-- QUESTION 2 -->
            <tab-content title="Habang bumabaha" icon="fa fa-info">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Habang bumabaha</h4>
                </div>
                <div class="panel-body">
                  <p>- Manatili sa loob ng bahay o evacuation area.</p>
                  <p>- Huwag lalangoy o mamangka sa mga ilog na umaapaw.</p>
                  <p>- Lumayo sa mga bumagsak na poste at iba pang mataas na bagay.</p>
                  <p>- Maging alerto sa gas leaks. Gamitin ang flashlight sa pag-iinspekto nito.</p>
                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 2 -->

            <!-- QUESTION 3 -->
            <tab-content title="Pagkatapos ng pag-baha" icon="fa fa-info">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Pagkatapos ng pag-baha</h4>
                </div>
                <div class="panel-body">
                  <p>- I-report ang putol na kawad/kable/tubo (kuryente, tubig, gas at telepono) sa kinauukulan.</p>
                  <p>- Bantayan ang mga bagay na pwedeng pagmulan ng sunog gaya ng mga putol na kawad ng kuryente.</p>
                  <p>- Huwag sindihan ang main switch o gumamit ng appliances na hindi pa nasusuri ng electrician.</p>
                  <p>- Huwag mamasyal o maki-usyoso sa lugar na tinamaan ng sakuna upang di makasagabal sa rescue at iba pang emergency operations.</p>
                </div>
              </div>
            </tab-content>
            <!-- END QUESTION 3 -->

            <!-- QUESTION 4 -->
            <!-- <tab-content title="Title 4" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Mga tanong (tama o mali)</h4>
                </div>
                <div class="panel-body">
                  
                </div>
              </div>
            </tab-content> -->
            <!-- END QUESTION 4 -->

            <!-- QUESTION 4 -->
            <!-- <tab-content title="Title 5" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Title05</h4>
                </div>
                <div class="panel-body">

                </div>
              </div>
            </tab-content> -->
            <!-- END QUESTION 5 -->

          </form-wizard>
        </div>
      </div>
    </div>
      

      <!-- ******** MODAL ******** -->
      <modal name="sunogModal" width="50%" height="auto" :scrollable="true">
        <div class="modal-content">
          <div class="modal-header">
            <button type="button" class="close" @click="closeModal" style="color:white;">&times;</button>
            <h4 class="modal-title"><i class="fa fa-question-circle"></i>&nbsp;Mga Tanong</h4>
          </div>
        </div>
        <div class="modal_body">
          <form action="" v-on:submit="submitBaha()">
            <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>1. Lumangoy sa baha. </p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-info">
                      <input type="radio" name="radio" id="radio1" @click="getAns1('tama')"/>
                      <label for="radio1">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio" id="radio2" @click="getAns1('mali')"/>
                      <label for="radio2">Mali</label>
                    </div>
                  </div>
                </div>
              </div>
          
              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>2. Dapat ba natin ipasuri  sa electrician ang mga bagay na nasira ng baha?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-info">
                      <input type="radio" name="radio1" id="radio3" @click="getAns2('tama')"/>
                      <label for="radio3">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio1" id="radio4" @click="getAns2('mali')"/>
                      <label for="radio4">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>3. Manatiling mahinahon at alerto.</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-info">
                      <input type="radio" name="radio2" id="radio5" @click="getAns3('tama')"/>
                      <label for="radio5">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio2" id="radio6" @click="getAns3('mali')"/>
                      <label for="radio6">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>4. Sumunod kaagad kapag inutos ng lokal na pamahalaan ang paglikas?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-info">
                      <input type="radio" name="radio3" id="radio7" @click="getAns4('tama')"/>
                      <label for="radio7">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio3" id="radio8" @click="getAns4('mali')"/>
                      <label for="radio8">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>5. Magtabi ng malinis na inuming tubig sa mga sisidlan bago pa dumating ang baha?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-info">
                      <input type="radio" name="radio4" id="radio9" @click="getAns5('tama')"/>
                      <label for="radio9">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio4" id="radio10" @click="getAns5('mali')"/>
                      <label for="radio10">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

              <div class="form-group row">
                <div class="col-md-12 col-xs-6">
                  <p>6. Kailangan ba natin ipaalam sa kinauukulang kung may putol na kable/tubo o kawad ?</p>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-info">
                      <input type="radio" name="radio5" id="radio11" @click="getAns6('tama')"/>
                      <label for="radio11">Tama</label>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-xs-6 col-sm-6">
                  <div class="funkyradio">
                    <div class="funkyradio-danger">
                      <input type="radio" name="radio5" id="radio12" @click="getAns6('mali')"/>
                      <label for="radio12">Mali</label>
                    </div>
                  </div>
                </div>
              </div>

                  <div class="button-container pull-right">
                    <button class="btn btn-success" type="submit"><i class="fa fa-check"></i>&nbsp;Isumite</button>
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
  props: ['cou'],
  data () {
    return {
      ans1: '',
      ans2: '',
      ans3: '',
      ans4: '',
      ans5: '',
      ans6: '',
      score: 0,
      coupon: 0
    }
  },
  components: {
    Navbar,
    FormWizard,
    TabContent
  },
  methods: {
    onCompleteBaha () {
      this.$modal.show('sunogModal')
    },
    closeModal () {
      this.$modal.hide('sunogModal')
    },
    submitBaha () {
      if (this.score >= 4) {
        this.$toastr.success('Nakakuha ka ng mataas na puntos', 'Puntos')
        this.$toastr.success('Naipasamo ang pagsusulit.', 'Ayos!')
        this.closeModal()
        this.$router.push('/lindol')
      }
      else {
        this.$toastr.success('Ang nakuha mong puntos ay mababa', 'Puntos')
        this.closeModal()
      }
    },
    getAns1 (n) {
      this.ans1 = n
      if (n === 'mali') {
        this.score += 1
      }
    },
    getAns2 (n) {
      this.ans1 = n
      if (n === 'tama') {
        this.score += 1
      }
    },
    getAns3 (n) {
      this.ans1 = n
      if (n === 'tama') {
        this.score += 1
      }
    },
    getAns4 (n) {
      this.ans1 = n
      if (n === 'mali') {
        this.score += 1
      }
    },
    getAns5 (n) {
      this.ans1 = n
      if (n === 'tama') {
        this.score += 1
      }
    },
    getAns6 (n) {
      this.ans1 = n
      if (n === 'tama') {
        this.score += 1
      }
    }
  }
}
</script>
<style scoped>
.bahaBody {
  background-image: url('/statics/baha-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  height: 650px;
  overflow: hidden;
}
.modal-header {
  background-color: #337ab7;
  color: white;
}
</style>

