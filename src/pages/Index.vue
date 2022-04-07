<template>
  <q-page style="overflow-x: hidden;">
    <div class="row" style="position: relative">
      <div class="col-12 main-background-color background-image">
        <div class="row justify-center items-center">
          <div class="col-auto first-section section-padding">
            <div class="text-center title">IMAGINE UM<br>LUGAR…</div>
            <div class="subtitle text-center">…onde você possa pertencer a um clube escolar, um grupo de gamers, ou uma comunidade artística mundial. Onde você e alguns amigos possam passar um tempo juntos. Um lugar que torna fácil conversar todos os dias e socializar com mais frequência.</div>
            <div class="flex flex-center q-mt-lg">
              <q-btn
                class="btn"
                style="text-transform: none"
                size="lg"
                color="white"
                text-color="black"
                unelevated
              >
                <q-icon name="mdi-download-outline" size="sm" class="q-mr-sm">
                </q-icon>
                Baixar para Windows
              </q-btn>
              <q-btn
                class="q-ml-md btn"
                style="text-transform: none; background-color: #23272a"
                text-color="white"
                size="lg"
                unelevated
              >
                Abrir o Discord no seu navegador
              </q-btn>
            </div>
          </div>
        </div>
      </div>
      <div class="col-12 first-section-background">
        <img class="img left" src="~assets/discord_left.svg" />
        <img class="img right" src="~assets/discord_right.svg" />
      </div>
    </div>
    <div class="row justify-center content-section" style="width: 100%;">
      <div>
        <div class="row justify-center align-center max-content-width section-padding">
          <div class="col-10 col-md-8">
            <img src="~assets/img1.svg" style="width: 100%; height: 100%"/>
          </div>
          <div class="col-10 col-md-4 text-col">
            <div class="title text-weight-bold">
              Crie um espaço controlado por convite onde você se sinta em casa
            </div>
            <div class="subtitle q-mt-lg">
              Os servidores Discord são organizados em canais com assuntos para vocês colaborarem, compartilharem ou simplesmente falarem do dia sem entupir um chat geral.
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-center content-section secondary-background-color" style="width: 100%;">
      <div>
        <div class="row justify-center align-center max-content-width section-padding">
          <div class="col-10 col-md-4 text-col">
            <div class="title text-weight-bold">
              Aqui é fácil se encontrar
            </div>
            <div class="subtitle q-mt-lg">
              Entre no canal de voz quando estiver à toa. Amigos no mesmo servidor podem te ver e entrar imediatamente, sem nem ter que fazer a chamada.
            </div>
          </div>
          <div class="col-10 col-md-8">
            <img src="~assets/img1.svg" style="width: 100%; height: 100%"/>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-center content-section" style="width: 100%;">
      <div>
        <div class="row justify-center align-center max-content-width section-padding">
          <div class="col-10 col-md-8">
            <img src="~assets/img1.svg" style="width: 100%; height: 100%"/>
          </div>
          <div class="col-10 col-md-4 text-col">
            <div class="title text-weight-bold">
              Para poucos e para muitos
            </div>
            <div class="subtitle q-mt-lg">
              Organize qualquer comunidade com ferramentas de moderação e acesso personalizado a membros. Dê poderes especiais aos membros, monte canais privados e muito mais.
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-center section-padding content-section" style="width: 100%;">
      <div class="col-auto">
        <div class="last-section-text text-center">
          <img class="stars" src="~assets/discord_stars.svg" />
          <div>Vamos começar sua jornada?</div>
        </div>
        <div class="flex flex-center">
          <q-btn
            class="btn discord-background-color q-mt-md"
            style="text-transform: none"
            size="lg"
            text-color="white"
            unelevated
          >
            <q-icon name="mdi-download-outline" size="sm" class="q-mr-sm">
            </q-icon>
            Baixar para Windows
          </q-btn>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageIndex'
})
</script>

<style scoped>
.title {
  font-size: 42px;
}

.subtitle {
  font-size: 16px;
}

.section-padding {
  padding: 120px 40px 120px 40px;
}

.content-section .title {
  max-width: 380px;
  line-height: 120%;
}

.content-section .subtitle {
  max-width: 380px;
}

.text-col {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.background-image {
  background-image: url('assets/discord_banner.svg');
  background-size: cover;
  background-position-x: center;
}

.first-section {
  z-index: 5;
}

.first-section .title {
  font-size: 56px;
  font-weight: 800;
  color: white;
  line-height: 95%;
}

.first-section .subtitle {
  font-size: 20px;
  font-weight: 400;
  color: white;
  max-width: 780px;
  line-height: 1.625;
  margin-top: 40px;
}

.first-section-background {
  position: absolute;
  bottom: 0;
  height: 100%;
}

.first-section-background .img {
  position: absolute;
  bottom: 0;
}

.first-section-background .left {
  right: 50%;
  margin-right: 350px;
}

.first-section-background .right {
  left: 50%;
  margin-left: 350px;
}

.btn {
  font-weight: 400;
  font-size: 18px !important;
  padding: 10px 25px 10px 25px;
  border-radius: 50px;
}

.last-section-text {
  position: relative;
  font-size: 32px;
  font-weight: bold;
}

.stars {
  position: absolute;
  margin-top: -20px;
  top: 0;
  left: -45px;
}

</style>
