<template>
  <v-app>
    <section class="back">
      <v-row no-gutters>
        <v-col lg="4" md="4" sm="12" cols="12">
          <div class="profile mx-md-5  my-md-3 my-xs-5 py-3">
            <v-row align="center" no-gutters>
              <v-col cols="4">
                <v-avatar class="ma-4">
                  <v-img src="/pic/avatar.png" class="avatar "> </v-img>
                </v-avatar>
              </v-col>

              <v-col cols="8" class="pl-md-3">
                <div class="head  textcol font-weight-black ">
                  Beverly Andrews
                </div>

                <div class="subtitle-1 white--text py-2">
                  User interface designer
                </div>

                <v-btn
                  fab
                  style="box-shadow: 0px 0px 20px rgba(187, 209, 244, 0.25);"
                  small
                >
                  <v-img
                    src="/pic/email.svg"
                    width="16"
                    height="16"
                    contain
                  ></v-img>
                </v-btn>
                <v-btn
                  fab
                  x-small
                  style="box-shadow: 0px 0px 20px rgba(187, 209, 244, 0.25);"
                  class="mx-2"
                >
                  <v-img
                    src="/pic/video-player.svg"
                    width="12"
                    height="12"
                    contain
                  ></v-img>
                </v-btn>
                <v-btn
                  fab
                  x-small
                  style="box-shadow: 0px 0px 20px rgba(187, 209, 244, 0.25);"
                >
                  <v-img
                    src="/pic/headphones.svg"
                    width="12"
                    height="12"
                    contain
                  ></v-img>
                </v-btn>
              </v-col>
            </v-row>
          </div>
        </v-col>
        <v-col lg="4" md="4" sm="12" justify="center" align-self="center">
          <div
            class="text-center text-md-subtitle-1 textcol font-weight-medium pb-md-4 hidden-xs-only"
          >
            Links to my profiles:
          </div>
          <div class="text-center mt-xs-6">
            <v-btn
              class="mx-md-2 mx-xs-3"
              fab
              small
              color="white"
              v-for="icon in icons"
              :key="icon.id"
              style="box-shadow: 0px 0px 25px #E4EAF4;"
            >
              <v-img width="16" height="16" contain :src="icon.src"></v-img>
            </v-btn>
          </div>
        </v-col>
        <v-col lg="3" md="3" sm="12" cols="12" class="ml-xl-12 mt-xl-4 mt-xs-8">
          <v-row justify-md="end" justify="center">
            <v-col cols="4" sm="3" md="3" lg="3">
              <div class="text-center textcol subtitle-1 font-light">
                Hourly rate
              </div>
              <div class="text-center textcol title font-weight-black">
                $25 USD
              </div>
            </v-col>
            <v-col cols="1">
              <div
                style="width:1px;height:2rem;background-color:#ED0000;"
                class="mt-xl-3"
              ></div>
            </v-col>

            <v-col cols="4" sm="3" md="3" lg="3">
              <div class="text-center textcol subtitle-1 font-light">
                Available for
              </div>
              <div class="text-center textcol title font-weight-black">
                8 hours
              </div>
            </v-col>
            <button class="hire py-5 mr-md-4 mt-6 ml-xs-12">
              <div class="text-center white--text font-weight-bold ">
                HIRE ME
              </div>
            </button>
          </v-row>
        </v-col>
      </v-row>
      <v-row class="mt-md-6 mt-xs-12 pt-xs-6">
        <v-col lg="10" sm="12" cols="12">
          <v-tabs
            background-color="transparent"
            class="tabhigh"
            hide-slider
            hide-arrows
            center-active
          >
            <v-tab
              v-for="tab in tabs"
              :key="tab.id"
              :to="tab.link"
              class="tab-button ml-md-5 mr-md-10 mx-xs-2 text-left "
              height
              exact-active-class
            >
              <v-btn fab class="iconsize" elevation="0" color="white">
                <v-img :src="tab.icon" width="16" height="16" contain></v-img>
              </v-btn>

              <div
                class="tabtitle font-weight-bold text-capitalize mx-md-4 ml-xs-2 mr-xs-5"
              >
                {{ tab.name }}
              </div>
            </v-tab>
          </v-tabs>
        </v-col>
      </v-row>
      <v-row>
        <v-col md="12" cols="12">
          <transition name="fade-up">
            <keep-alive>
              <router-view></router-view>
            </keep-alive>
          </transition>
        </v-col>
      </v-row>
    </section>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
      activetab: 1,
      tablet: null,
      icons: [
        {
          id: 1,
          src: "/pic/behance.svg"
        },
        {
          id: 2,
          src: "/pic/dribbble.svg"
        },
        {
          id: 3,
          src: "/pic/instagram.svg"
        },
        {
          id: 4,
          src: "/pic/linkedin.svg"
        },
        {
          id: 5,
          src: "/pic/google-plus.svg"
        }
      ],
      tabs: [
        {
          id: 1,
          name: "Portfolio",
          icon: "/pic/portfolio.svg",
          link: "/"
        },
        {
          id: 2,
          name: "Work",
          icon: "/pic/work.svg",
          link: "/work"
        },
        {
          id: 3,
          name: "Education",
          icon: "/pic/education.svg",
          link: "/education"
        },
        {
          id: 4,
          name: "Skills",
          icon: "/pic/skills.svg",
          link: "/skills"
        }
      ]
    };
  }
};
</script>
<style >

.v-tabs-bar{
  height: 60px !important;
}
.textcol {
  color: #222D68 !important;
}
body{

  background: linear-gradient(125.55deg, #FFFFFF 10.06%, #FFFFFF 75.33%);

}
.back{
    background-image: url('/pic/backdesign.svg');
    background-size: cover;
    background-repeat: no-repeat;
    
  }

.profile{
    background: linear-gradient(97.67deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);
    box-shadow: 0px 4px 20px rgba(253, 191, 187, 0.44);
    border-radius: 10px 10px 200px 10px;
  }
.tab-button{
  background: linear-gradient(99.48deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);
  opacity: 0.4;
  box-shadow: 0px 4px 20px rgba(253, 191, 187, 0.44);
  border-radius: 5px 5px 60px 5px;
  width: 14rem;
 color:#222D68 !important;
 
}
.theme--light.v-tabs .v-tab:hover {

 border-radius: 5px 5px 60px 5px !important;
 color:#222D68 !important;
}
.theme--light.v-tabs .v-tab--active:before, .theme--light.v-tabs .v-tab--active:hover:before, .theme--light.v-tabs .v-tab:focus:before {
    opacity: 0 !important;
}
.v-tab--active{
  opacity: 1;
  color:#222D68 !important;
}

  .fade-up-enter-active,
  .fade-up-leave-active {
    transition: all 0.3s ease-in-out;
  }
  .fade-up-enter,
  .fade-up-leave-to {
   
    transform: translateX(30px);
    opacity: 0;
  }
  .hire{
    background: linear-gradient(99.68deg, #F9BFDA 1.07%, #FFCAD0 51.95%, #FDBEBA 89.88%);
    box-shadow: 0px 4px 20px rgba(253, 191, 187, 0.44);
    border-radius: 60px 5px 5px 5px;
    width: 14rem;
  }
  .v-avatar{
    width: 10rem !important;
    height: 10rem !important;
  }
  .head{
    font-size: 1.5rem;
  }
  .tabtitle{
    font-size: 1.5rem;
  }
  .iconsize{
    width: 32px !important;
    height: 32px !important;
  }
@media only screen and (max-width: 600px) {
  .v-avatar{
    width: 6rem !important;
    height: 6rem !important;
  }
  .profile{
    margin: 0px 6px;
  }
  .v-tabs-bar.v-slide-group--is-overflowing.v-tabs-bar--is-mobile:not(.v-tabs-bar--show-arrows):not(.v-slide-group--has-affixes) .v-slide-group__prev {
    display: none !important;
    visibility: hidden;
  }
  .v-tabs-bar{
    height: 45px !important;
  }
  .tab-button{
  
    width: 10rem !important;
  
  
  }
  .tabtitle{
      font-size: 1rem;
    }
  }
.iconsize{
    width: 32px !important;
    height: 32px !important;
  }
</style>
