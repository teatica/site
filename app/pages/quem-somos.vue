<template>
  <div class="white">
    <Banner txt1="QUEM" txt2="SOMOS"></Banner>
    <div class="spa-24 spt-xs-24 spx-xs-10 spb-xs-10">
      <p class="spx-sm-24 spx-xs-0 text-center">
        <big
          >A Associação Multiversa Internacional é uma associação comunitária,
          sem fins lucrativos e filantrópica, fundada em setembro de 2013 por um
          grupo de educadores cuja missão é difundir a APRENDIZAGEM EVOLUTIVA no
          Brasil e no exterior.
        </big>
      </p>
      <p class="spx-sm-24 spx-xs-15 spb-10 text-center">
        <big
          >A associação possui diversas frentes de atuação social, entre
          elas</big
        >
        estão:
      </p>
      <HomeProdutosItems></HomeProdutosItems>
    </div>

    <v-layout class="spy-24 grey lighten-3 flex-wrap">
      <v-flex xs12 md4 lg3 class="spl-24 spx-xs-15">
        <p>
          A Associação Multiversa Internacional é composta por um
          <span class="font-600"> Conselho Deliberativo </span>, um
          <span class="font-600">Conselho Fiscal</span> e uma
          <span class="font-600">Diretoria Executiva</span>, formada pelas
          seguintes pessoas:
        </p>
      </v-flex>
      <v-flex xs12 md8 lg9 class="spx-sm-24 spx-xs-15 pt-2">
        <div data-aos="fade-right" data-aos-delay="250">
          <span class="c-primary spx-3 spy-1 d-inline">
            <p class="d-inline font-800 c-secondary--text">
              CONSELHO DELIBERATIVO
            </p>
          </span>
          <v-layout class="flex-wrap mt-10">
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5"
                  :src="$imagine('/staff/ryon.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Ryon Braga</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/cristina.png')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Cristina Dalvi Davel</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/lucia.png')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Lúcia Helena Makhlouf</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/djalma.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">José Djalma Cajado da Fonseca</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/norma.png')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Norma Viapiana Golfeto</p>
              </v-flex>
            </v-flex>
          </v-layout>
          <br />
          <br />
        </div>
        <div data-aos="fade-right" data-aos-delay="500">
          <span class="c-primary spx-3 spy-1 d-inline">
            <p class="d-inline font-800 c-secondary--text">CONSELHO FISCAL</p>
          </span>

          <v-layout class="flex-wrap mt-10">
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/graca.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Graça Souza</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/otavio.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Otávio Augusto Araújo</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/izabel.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Maria Izabel Conceição</p>
              </v-flex>
            </v-flex>
          </v-layout>
          <br />
          <br />
        </div>
        <div data-aos="fade-right" data-aos-delay="750">
          <span class="c-primary spx-3 spy-1 d-inline">
            <p class="d-inline font-800 c-secondary--text">
              DIRETORIA EXECUTIVA
            </p>
          </span>
          <v-layout class="flex-wrap mt-10">
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5"
                  :src="$imagine('/staff/ryon.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">Ryon Braga</p>
              </v-flex>
            </v-flex>
            <v-flex xs6 lg4 class="d-flex align-center flex-wrap smb-8">
              <v-flex xs12 md5>
                <v-img
                  style="border-radius: 300px"
                  class="smr-5 c-info"
                  :src="$imagine('/staff/djalma.jpg')"
                ></v-img>
              </v-flex>
              <v-flex>
                <p class="font-600">José Djalma Cajado da Fonseca</p>
              </v-flex>
            </v-flex>
          </v-layout>
        </div>
        <br />
        <br />
        <br />
        <br />
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {}
// export default {
//   async asyncData({ $http }) {
//     const blogs = JSON.parse(await $http.$get('/blog/index.json'))

//     return { blogs }
//   },
// }
</script>

