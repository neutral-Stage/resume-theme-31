<template>
  <v-app>
    <v-container>
      <v-row justify="center" align="center" class="mt-12">
        <v-col
          md="4"
          cols="12"
          sm="12"
          class="px-md-6 px-xs-0"
          v-for="img in images"
          :key="img.id"
        >
          <v-img :src="img.src"> </v-img>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          id: 1,
          src: "/pic/img1.png"
        },
        {
          id: 2,
          src: "/pic/img2.png"
        },
        {
          id: 3,
          src: "/pic/img3.png"
        },
        {
          id: 4,
          src: "/pic/img4.png"
        },
        {
          id: 5,
          src: "/pic/img5.png"
        },
        {
          id: 6,
          src: "/pic/img6.png"
        }
      ]
    };
  }
};
</script>

<style >
.theme--light.v-application {
  background: transparent;
  color: rgba(0, 0, 0, 0.87);
}
.navblade {
  position: relative;
  background-color: #104efb;
  border-top-left-radius: 300px;
  border-bottom-left-radius: 0;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
</style>
