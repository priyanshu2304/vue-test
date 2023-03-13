<template>
  <div><BottomSheetVue v-if="showBottomSheet" @close="bottomSheet" /></div>
</template>

<script>
import BottomSheetVue from './common/BottomSheet.vue'

export default {
  data() {
    return {
      showBottomSheet: null,
    }
  },
  components: {
    BottomSheetVue,
  },
  mounted(){
    this.showBottomSheet = true 
  },
  methods: {
    bottomSheet() {
      this.showBottomSheet = false
    },
  },
}
</script>

<style lang="scss" scoped></style>
