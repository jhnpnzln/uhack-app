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
            <tab-content title="Title 4" icon="fa fa-question">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h4 class="panel-title">Mga tanong (tama o mali)</h4>
                </div>
                <div class="panel-body">
                  <p>1. Lumangoy sa baha. </p>
                  <div><input type="radio" name="baha1">Tama</input>
                  <input type="radio" name="baha1">Mali</input></div>
                  <p>2. Dapat ba natin ipasuri  sa electrician ang mga bagay na nasira ng baha?</p>
                  <div><input type="radio" name="baha2">Tama</input>
                  <input type="radio" name="baha2">Mali</input></div>
                  <p>3. Manatiling mahinahon at alerto.</p>
                  <div><input type="radio" name="baha3">Tama</input>
                  <input type="radio" name="baha3">Mali</input></div>
                  <p>4. Sumunod kaagad kapag inutos ng lokal na pamahalaan ang paglikas?</p>
                  <div><input type="radio" name="baha4">Tama</input>
                  <input type="radio" name="baha4">Mali</input></div>
                  <p>5. Magtabi ng malinis na inuming tubig sa mga sisidlan bago pa dumating ang baha?</p>
                  <div><input type="radio" name="baha5">Tama</input>
                  <input type="radio" name="baha5">Mali</input></div>
                  <p>6. Kailangan ba natin ipaalam sa kinauukulang kung may putol na kable/tubo o kawad ?</p>
                  <div><input type="radio" name="baha6">Tama</input>
                  <input type="radio" name="baha6">Mali</input></div>
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
  },
  methods: {
    onCompleteBaha () {
      this.$toastr.success('Naisumite na.', 'Ayos!')
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
</style>

