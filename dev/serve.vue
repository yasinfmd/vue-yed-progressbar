<script>
import Vue from 'vue';
import VueYedProgressbar from '@/vue-yed-progressbar.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueYedProgressbar
  }
});
</script>

<template>
  <div id="app">
    <vue-yed-progressbar />
  </div>
</template>
