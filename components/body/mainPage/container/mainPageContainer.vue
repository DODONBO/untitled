<template>
  <div>
    <MainPageVisual/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import {library} from "@fortawesome/fontawesome-svg-core";
import { fas } from "@fortawesome/free-solid-svg-icons";
import { far } from "@fortawesome/free-regular-svg-icons";
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
import {Component} from "vue-property-decorator";
import MainPageVisual from '../mainPageVisual.vue';


library.add(fas, far)
Vue.component('font-awesome-icon', FontAwesomeIcon)
Vue.config.productionTip = false

@Component({
  components: {MainPageVisual}
})
export default class MainPageContainer extends Vue {
}
</script>
