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
          <form-wizard color="#1abc9c" title="Bagyo" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may bagyo."
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


              <tab-content title="Mga tanong(tama o mali)" icon="fa fa-info">
              <div class="panel panel-turquoise">
              <div class="panel-heading">
                <h4 class="panel-title">
                 
                </h4>
              </div>
              <div class="panel-body">
                   <p>1. Makinig sa radyo o manood sa telebisyon tungkol sa weather updates</p>
                    <input type="radio" name="question1"    value="Tama" >Tama
                    <input type="radio" name="question1"   value="Mali" >Mali
                    <p>2. Natiyak ba nating ang kable o outlet ay sakaling nakababad sa tubig?</p>
                     <input type="radio" name="question2"    value="Tama" >Tama
                    <input type="radio" name="question2"   value="Mali" >Mali
                    <p>3. Nasuri mo ang iyong bahay kung ito ba ay matibay ,Manatili sa loob ng bahay? </p>
                     <input type="radio" name="question3"    value="Tama" >Tama
                    <input type="radio" name="question3"   value="Mali" >Mali
                    <p>4. Mangisda sa kasagsagan ng bagyo?</p>
                     <input type="radio" name="question4"    value="Tama" >Tama
                    <input type="radio" name="question4"   value="Mali" >Mali
                    <p>5. Maghanda ng ilawan at radyong de baterya</p>
                     <input type="radio" name="question5"    value="Tama" >Tama
                    <input type="radio" name="question5"   value="Mali" >Mali
               </div>
            </div>
            </tab-content>
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
.bagyoBody {
  background-image: url('/statics/bagyo-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  height: 650px;
  overflow: hidden;
}
</style>


