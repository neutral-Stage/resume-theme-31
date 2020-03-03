<template>
  <v-app>
    <v-row justify="center" class="mt-12">
      <v-col md="10" sm="12">
        <v-row justify="center">
          <v-col md="6" sm="12" cols="12" v-for="n in 4" :key="n">
            <v-row
              justify="center"
              class="layer ma-md-4 py-md-6 ma-xs-1 py-xs-3"
              no-gutters
            >
              <v-col cols="12" md="12" class="pl-md-6 pl-xs-3">
                <v-btn
                  fab
                  elevation="0"
                  class="workicon"
                  style="background: linear-gradient(92.67deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);"
                >
                  <v-img :src="temp.icon" class="iconimg" contain></v-img>
                </v-btn>
                <v-row
                  class="pl-md-12 ml-12 mt-xs-n8 pl-xs-6 mt-md-4"
                  no-gutters
                >
                  <v-col md="12" sm="12" cols="12">
                    <h1 class="textcol headline font-weight-bold">
                      {{ temp.title }}
                    </h1>
                  </v-col>
                  <v-row no-gutters class="pr-6 mt-md-8 pb-6 mt-xs-2">
                    <v-col md="6" sm="6" cols="12" class="my-xs-4">
                      <h1
                        class="subtitle-2 font-weight-bold "
                        style="color:#F97CB3;"
                      >
                        {{ temp.duration }}
                      </h1>
                    </v-col>
                    <v-col
                      md="3"
                      sm="3"
                      cols="3"
                      class="text-center pr-12 hidden-xs-only"
                    >
                      <h1 class=" subtitle-2 pb-2 mr-12" style="color:#F97CB3;">
                        {{ temp.sub }}
                      </h1>
                    </v-col>
                    <v-col
                      md="8"
                      sm="8"
                      cols="12"
                      class="px-md-12 pb-12 pr-xs-0"
                    >
                      <h1 class="textcol sfont pb-2 font-weight-thin ">
                        {{ temp.para }}
                      </h1>
                    </v-col>
                  </v-row>
                </v-row>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      temp: {
        icon: "/pic/education.svg",
        title: "California Institute of Technology",
        sub: "University",
        duration: "M.Sc in HCI, Dec 19 - Present",
        para:
          "I'm a paragraph. Click here to add your own text and edit me. It’s easy. Just click “Edit Text” or double click me to add your  and make changes."
      }
    };
  }
};
</script>

<style scoped>
.sfont{
  font-size: 0.70rem;
}
.theme--light.v-application {
  background: transparent;
  color: rgba(0, 0, 0, 0.87);
}
  .layer
  {
    background: #FFFFFF;
    box-shadow: 0px 0px 25px #E4EAF4;
    border-radius: 20px 20px 260px 20px;
  }
.textcol {
  color: #222D68 !important;
}
@media only screen and (max-width: 600px) {
  .workicon{
  height: 40px !important;
  width: 40px !important;
  }
  .iconimg{
    height: 18px !important;
    width: 18px !important;
  }
  .layer
  {
    background: #FFFFFF;
    box-shadow: 0px 0px 25px #E4EAF4;
    border-radius: 20px 20px 140px 20px !important;
  }
.sfont{
  font-size: 0.80rem;
}
}
</style>
