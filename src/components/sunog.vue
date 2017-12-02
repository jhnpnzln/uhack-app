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
          <form-wizard  color="#e74c3c" title="Sunog" subtitle="Mga bagay na dapat gawin at hindi dapat gawin tuwing may sunog."
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

          
            <!-- PANEL 05 -->
            <tab-content title="Katanungan" icon="fa fa-question">
              <div class="panel panel-red">
                <div class="panel-heading">
                  <h4 class="panel-title"> Mga tanong(tama o mali)</h4>
                </div>
                <div class="panel-body">
                  <p>1.Nainspekyun na ng kinauukulan ang iyong bahay?</p>
                  <input type="radio" name="question1">Tama
                  <input type="radio" name="question1">Mali
                  <p>2.Tumawag ng bumbero. </p>
                    <input type="radio" name="question2">Tama
                  <input type="radio" name="question2">Mali
                  <p>3.Aalisin ba natin ang mga bagay na pedeng mag bigay ng karagdagang sunog?</p>
                    <input type="radio" name="question3">Tama
                  <input type="radio" name="question3">Mali
                  <p>4.Ibaba ang main switch. </p>
                    <input type="radio" name="question4">Tama
                  <input type="radio" name="question4">Mali
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
