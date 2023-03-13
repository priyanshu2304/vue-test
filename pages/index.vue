<template>
  <div class="test__container">
    <div v-if="deviceType === 'desktop'">
      <MainHeader />
      <div class="test__container-section"><SideBarDesktop /><MainBody /></div>
    </div>
    <div v-else>
      <div class="test__container-mobile"><MainHeader /><MainBodyMobileVue /></div>
    </div>
  </div>
</template>

<script>
import MainHeader from '~/components/MainHeader.vue'
import MainBody from '~/components/MainBody.vue'
import SideBarDesktop from '~/components/SideBarDesktop.vue'
import MainBodyMobileVue from '~/components/MainBodyMobile.vue'
export default {
  components: { MainHeader, SideBarDesktop, MainBody, MainBodyMobileVue },
  name: 'IndexPage',
  data() {
    return {
      deviceType: '',
    }
  },

  mounted() {
    this.getDeviceType()
    window.addEventListener('resize', this.getDeviceType)
  },

  methods: {
    getDeviceType() {
      if (window.innerWidth <= 480) {
        this.deviceType = 'mobile'
      } else {
        this.deviceType = 'desktop'
      }
    },
  },
}
</script>

<style>
.test__container {
  display: flex;
  flex-direction: column;
}

.test__container-section {
  display: flex;
  justify-content: row;
}

body {
  margin: 0px;
}

.test__container-mobile {
  display: flex;
  justify-content: row;
}
</style>
