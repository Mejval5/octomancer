
<template>
  <v-expand-x-transition>
    <v-container
      class="pa-0 ma-0 fill-height"
      :style="get_height_dirty"
      fluid
    >
      <div
        class="rounded-0"
        style="overflow: hidden; height: 100%; width: 100%; max-width: 1600px; margin: auto; margin: auto; z-index: 1600; position:static;"
      >
        <div
          class="rounded-0"
          style="height: 100%;  width: 100%; overflow: hidden; "
        >
          <v-row
            v-show="expand"
            v-resize="onResize"
            class="align-center ma-0"
            justify="center"
            align="center"
            style=" height: 100%; width: 100%;"
          >
            <v-col
              class="pa-0"
              cols="12"
              style="display: block; height: 100%;"
            >
              <div
                class="parent"
                :style="get_mobile_size"
              >
                <div class="child">
                  <div
                    id="scene"
                    data-relative-input="true"
                    class="scene"
                  >
                    <div
                      id="bg1"
                      data-depth="0.30"
                      style="position:relative !important;"
                    >
                      <img
                        :src="require('@/assets/milan/1.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg2"
                      data-depth="0.30"
                    >
                      <img
                        :src="require('@/assets/milan/2.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg3"
                      data-depth="0.33"
                    >
                      <img
                        :src="require('@/assets/milan/3.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg4"
                      data-depth="0.36"
                    >
                      <img
                        :src="require('@/assets/milan/4.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg5"
                      data-depth="0.39"
                    >
                      <img
                        :src="require('@/assets/milan/5.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg6"
                      data-depth="0.42"
                    >
                      <img
                        :src="require('@/assets/milan/6.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg7"
                      data-depth="0.45"
                    >
                      <img
                        :src="require('@/assets/milan/7.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg8"
                      data-depth="0.48"
                    >
                      <img
                        :src="require('@/assets/milan/8.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg9"
                      data-depth="0.51"
                    >
                      <img
                        :src="require('@/assets/milan/9.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg10"
                      data-depth="0.54"
                    >
                      <img
                        :src="require('@/assets/milan/10.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg11"
                      data-depth="0.57"
                    >
                      <img
                        :src="require('@/assets/milan/11.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg12"
                      data-depth="0.60"
                    >
                      <img
                        :src="require('@/assets/milan/12.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg13"
                      data-depth="0.63"
                    >
                      <img
                        :src="require('@/assets/milan/13.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg14"
                      data-depth="0.66"
                    >
                      <img
                        :src="require('@/assets/milan/14.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg15"
                      data-depth="0.69"
                    >
                      <img
                        :src="require('@/assets/milan/15.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg16"
                      data-depth="0.72"
                    >
                      <img
                        :src="require('@/assets/milan/16.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg17"
                      data-depth="0.75"
                    >
                      <img
                        :src="require('@/assets/milan/17.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg18"
                      data-depth="0.78"
                    >
                      <img
                        :src="require('@/assets/milan/18.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg19"
                      data-depth="0.81"
                    >
                      <img
                        :src="require('@/assets/milan/19.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <!--<div data-depth="0.3" class="border"></div>-->
                    <div
                      id="bg20"
                      data-depth="0.84"
                    >
                      <img
                        :src="require('@/assets/milan/20Overlay.png')"
                        width="120%"
                        style="margin-left:-10%;margin-top:-10%;"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg21"
                      data-depth="0.84"
                      class="bg20"
                    >
                      <img
                        :src="require('@/assets/milan/20.png')"
                        width="100%"
                        class="gg"
                      >
                    </div>
                    <div
                      id="bg22"
                      data-depth="0.84"
                      class="bgLight"
                    >
                      <img
                        :src="require('@/assets/milan/Light.png')"
                        width="100%"
                        class="gg gg1"
                      >
                    </div>
                    <!--    <div
                      id="bg23"
                      class="menu1 primaryText"
                      style="opacity: 1; text-shadow: 0 0 1vh rgba(255,255,255,0.0);"
                    >
                      <p><a>OCTOMANCER</a> <br><br> <a>BROTAGONISTS™</a> <br><br> <a>SUPPORT US</a> <br><br> <a>CONTACT</a></p>
                    </div> -->
                  </div>
                </div>
              </div>
              <base-scrolling-item />
            </v-col>
          </v-row>
          <v-row
            v-show="!expand"
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            />
          </v-row>
        </div>
      </div>
    </v-container>
  </v-expand-x-transition>
</template>

<script>
  import Parallax from '@/plugins/parallax.js'
  import DanParallax from '@/plugins/danparallax.js'

  // Extensions
  import View from '@/views/View'

  // Mixins
  import LoadSections from '@/mixins/load-sections'

  export default {

    name: 'Octomancer',

    extends: View,

    props: {
      id: {
        type: String,
        default: 'octomancer',
      },
    },

    data: () => ({
      expand: false,
      parallaxInstance: {},
    }),

    computed: {
      get_mobile_size () {
        if (this.$vuetify.breakpoint.smAndDown) {
          return 'width: 2560px;'
        } else if (this.$vuetify.breakpoint.mdAndUp && this.$vuetify.breakpoint.lgAndDown) {
          return 'width: 2560px;'
        } else {
          return 'width: 2560px;'
        }
      },
      get_height_dirty () {
        var height = this.$vuetify.breakpoint.mdAndUp ? 'calc(100vh - 90px)' : 'calc(100vh - 118px)'
        return 'max-height: ' + height + ';'
      },
    },

    beforeRouteUpdate (to, from, next) {
      console.log(to)
      console.log(from)
      console.log(next)
    },

    mounted () {
      var scene = document.getElementById('scene')
      // this.parallaxInstance = new Parallax(scene)
      this.$nextTick(() => {
        this.show_image()
      })
    },

    created () {
      window.addEventListener('beforeunload', this.stop_anim)
    },

    beforeRouteLeave (to, from, next) {
      this.stop_anim()
      next()
    },

    methods: {
      stop_anim () {
        this.parallaxInstance.methods.stop = true
        window.removeEventListener('beforeunload', this.stop_anim)
      },
      async show_image () {
        this.parallaxInstance = await new DanParallax()
        await new Promise(resolve => setTimeout(resolve, 200))
        this.expand = true
        this.parallaxInstance.methods.run()
        // console.log(this.parallaxInstance)
      },
      onResize (event) {
        try {
          if (this.$vuetify.breakpoint.mdAndUp && !this.parallaxInstance.enabled) {
            this.parallaxInstance.enableThisF()
          }
          if (!this.$vuetify.breakpoint.mdAndUp && this.parallaxInstance.enabled) {
            this.parallaxInstance.disableThisF()
          }
        } catch {}
      },
      firstLoad () {
        if (this.$vuetify.breakpoint.mdAndUp) {
          this.parallaxInstance.enableThisF()
        }
        if (!this.$vuetify.breakpoint.mdAndUp) {
          this.parallaxInstance.disableThisF()
        }
        console.log(this.parallaxInstance)
        console.log(this.$vuetify.breakpoint.mdAndUp)
      },
    },

    metaInfo: { title: 'Octomancer' },
  }
  </script>

<style scoped>
@charset "utf-8";
/* CSS Document */
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');

body {background-color:#e0e0e0;}
body {background-color:rgba(8,18,20,1);color: white;font-family: 'Quicksand', sans-serif;}

.parent {
position: relative;
z-index: 997;
min-width: 800px;
width: 150vw;
top: 50%;
margin-left: 50%;
transform: translate(-50%, -50%);
}

.child {
width:100%;
height:auto;
z-index: 998;
pointer-events: none;
}

.scene {
width:100%;
height:100%;
}

/*.border {
width: 100%;
height: 100%;
background-color:#e0e0e0;
    box-shadow: 0 0 0 10vw black;
}*/

.mybg {
    position: absolute;
    display: block;
    left: 0px;
    top: 0px;
    transform: translate(0px, 0px)
}

.bg20 {
outline: 1000px solid rgba(8,18,20,1);
}

.fixedMenu{
width: 100%;
height: 200px;
background-color: #e0e0e0;
z-index: 999;
}
.menu1
{
width: 100%;
text-align: center;
}
.menuItemName
{
font-size: 2vh;
font-weight: 700;
position: relative;
z-index: 999!important;
pointer-events: auto;
opacity: 1;
text-shadow: 0 0 1vh rgba(255,255,255,0.0);
}

.menu1 p {
font-size: 2vh;
padding-top: 23%;
font-weight: 700;
position: relative;
z-index: 999!important;
pointer-events: auto;
}

a {
text-decoration: none;
cursor: pointer;
color: inherit;
}
.elevation-n1 {
  box-shadow: inset 0px 0px 100px 100px black !important;
}
</style>
