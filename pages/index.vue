<template>
  <div>
    <HeaderContainer/>
    <MainPageContainer/>
    <div style="height: 600px;"></div>
  </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator'
import HeaderContainer from '~/components/header/container/headerContainer.vue';
import MainPageContainer from "~/components/body/mainPage/container/mainPageContainer.vue";

import 'assets/css/style.css';
import 'assets/css/font.css';
@Component({
  components: {MainPageContainer, HeaderContainer}
})
export default class Index extends Vue {

}
</script>
