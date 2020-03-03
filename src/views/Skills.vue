<template>
  <v-app>
    <v-row no-gutters justify="center" class="mt-10">
      <v-col md="8" lg="10">
        <v-tabs
          v-model="tab"
          background-color="transparent"
          height="60"
          color="#222D68"
          center-active
          hide-arrows
          grow
        >
          <v-tabs-slider style="height:0px;padding:0 0 !important;">
          </v-tabs-slider>
          <v-tab
            v-for="item in items"
            :key="item.id"
            exact
            class="subtitle-1 text-capitalize "
            active-class="font-weight-bold"
          >
            {{ item.name }}
          </v-tab>
        </v-tabs>

        <v-row no-gutters class="mt-12">
          <v-col md="12" sm="12" cols="12">
            <v-tabs-items v-model="tab" style="background-color:transparent;">
              <v-tab-item v-for="item in items" :key="item.id">
                <v-row class="justify-start py-2" align="center" no-gutters>
                  <v-col
                    xl="5"
                    lg="5"
                    md="5"
                    sm="12"
                    cols="12"
                    v-for="(s, index) in item.skills"
                    :key="index"
                    class="px-md-6 mx-md-6 my-6 px-xs-2 mx-xs-2"
                  >
                    <v-row no-gutters class="ml-12 mb-n2">
                      <v-col
                        ><div class="skilltext textcol ">
                          {{ s.name }}
                        </div></v-col
                      >
                      <v-col
                        ><div class="skilltext textcol text-right mr-3">
                          {{ s.val }}
                        </div></v-col
                      >
                    </v-row>

                    <v-btn
                      class="mx-2 btnborder"
                      fab
                      dark
                      small
                      elevation="0"
                      style="border: 4px solid #FDBFBC !important;z-index:999;"
                      color="#222D68"
                    >
                      <div class="title text-lowercase white--text">
                        {{ s.icon }}
                      </div>
                    </v-btn>
                    <div class="pro-back mt-n7 ml-11 mr-xs-3">
                      <div class="progress" style="width:70%;"></div>
                    </div>
                  </v-col>
                </v-row>
              </v-tab-item>
            </v-tabs-items>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "skills",
  data() {
    return {
      tab: null,
      items: [
        {
          id: 1,
          name: "Programming Languages",
          skills: [
            {
              name: "Photoshop",
              val: "90%",
              icon: "ph"
            },

            {
              name: "Illustrator",
              val: "80%",
              icon: "ill"
            },

            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            },
            {
              name: "Photoshop",
              val: "90%",
              icon: "ph"
            },

            {
              name: "Illustrator",
              val: "80%",
              icon: "ill"
            },

            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            }
          ]
        },
        {
          id: 2,
          name: "Frameworks/ Databases",
          skills: [
            {
              name: "Photoshop",
              val: "90%",
              icon: "ph"
            },
            {
              name: "Illustrator",
              val: "80%",
              icon: "ill"
            },

            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            },
            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            }
          ]
        },
        {
          id: 3,
          name: "Design Skills",
          skills: [
            {
              name: "Photoshop",
              val: "90%",
              icon: "ph"
            },
            {
              name: "Photoshop",
              val: "90%",
              icon: "ph"
            },

            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            },
            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            }
          ]
        },
        {
          id: 4,
          name: "Software",
          skills: [
            {
              name: "Photoshop",
              val: "90%",
              icon: "ph"
            },

            {
              name: "Figma",
              val: "75%",
              icon: "fig"
            }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
.skilltext{
  font-size: 1.50rem !important;
}
.pro-back{
  background: #E4E4E4;
opacity: 0.7;
border-radius: 15px;
max-width: 100%;
z-index: 10;
}
.progress{
  height:15px;
  background: linear-gradient(138.05deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);
  border-radius: 15px;
}
.textcol {
  color: #222D68 !important;
}
.v-tabs {
  position: relative;
}
.v-tabs:after {
  content: "";
  position: absolute;
  height: 2px;
  width: 90%;
  background-color: rgba(34, 45, 104, 0.1);

  margin: 0 50px 0 50px;
  bottom: 0;
}
.v-tabs .v-tab--active:after{
content: "";
  position: absolute;
  height: 5px;
  width: 30%;
 background: linear-gradient(151.48deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);
border-radius: 15px;

  margin: auto;
  bottom: 0;
}
.theme--light.v-application {
  background: transparent;
  color: rgba(0, 0, 0, 0.87);
}

.basil--text {
  color: #104efb !important;
}
.margleft {
  margin-left: 24px;
}
@media only screen and (max-width: 600px) {
  .v-tabs-bar.v-slide-group--is-overflowing.v-tabs-bar--is-mobile:not(.v-tabs-bar--show-arrows):not(.v-slide-group--has-affixes) .v-slide-group__prev {
    display: none !important;
    visibility: hidden;
  }
    .v-tabs .v-tab--active:after{
  content: "";
    position: absolute;
    height: 5px;
    width: 40%;
    left: 16px;
  background: linear-gradient(151.48deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);
  border-radius: 15px;

    margin: auto;
    bottom: 0;
  }
  .v-tabs--grow > .v-tabs-bar .v-tab {
      -webkit-box-flex: 1;
      -ms-flex: 1 0 auto;
      flex: 1 0 auto;
      max-width: 20% !important;
      
      text-align: left !important;
  }
  .theme--light.v-tabs>.v-tabs-bar .v-tab:not(.v-tab--active), .theme--light.v-tabs>.v-tabs-bar .v-tab:not(.v-tab--active)>.v-icon {
     max-width: 20% !important;
  }
 .skilltext{
  font-size: 1rem !important;
  }
}
</style>
