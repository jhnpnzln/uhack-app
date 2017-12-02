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
          <form-wizard color="#e67e22" title="Lindol" subtitle="Mga dapat gawin bago, habang at pagkatapos ng lindol."
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

            <!-- PANEL 04 -->
            <tab-content title="Title 1" icon="fa fa-question">
              <div class="panel panel-yellow">
                <div class="panel-heading">
                  <h4 class="panel-title">Mga tanong (tama o mali)</h4>
                </div>
                <div class="panel-body">
                  <p>1. Magwalang bahala, matatapos din yan..  </p>
                  <div><input type="radio" name="lindol1">Tama</input>
                  <input type="radio" name="lindol1">Mali</input></div>
                  <p>2. Iiwasan natin ang malapit sa dagat ?</p>
                  <div><input type="radio" name="lindol2">Tama</input>
                  <input type="radio" name="lindol2">Mali</input></div>
                  <p>3. Alamin ang earthquake plan sa bahay, opisina o paaralan.</p>
                  <div><input type="radio" name="lindol3">Tama</input>
                  <input type="radio" name="lindol3">Mali</input></div>
                  <p>4. Magtago sa ilalim ng lamesa. </p>
                  <div><input type="radio" name="lindol4">Tama</input>
                  <input type="radio" name="lindol4">Mali</input></div>
                  <p>5. Ihahanda ba natin ang ating sarili dulot ng lindol?</p>
                  <div><input type="radio" name="lindol5">Tama</input>
                  <input type="radio" name="lindol5">Mali</input></div>
                  <p>6. Patayin ang kuryente, tubig, at gas kapag nagbigay ng babala ang lokal na pamahalaan?</p>
                  <div><input type="radio" name="lindol6">Tama</input>
                  <input type="radio" name="lindol6">Mali</input></div>
                </div>
              </div>
            </tab-content>
            <!-- END PANEL 04 -->

            <!-- PANEL 05 -->
            <tab-content title="Title 1" icon="fa fa-question">
              <div class="panel panel-yellow">
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
.lindolBody {
  background-image: url('/statics/lindol-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  height: 650px;
  overflow: hidden;
}
</style>
