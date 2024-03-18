<template>
  <HeaderContainer/>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator'
import HeaderContainer from '~/components/header/container/headerContainer.vue';

import 'assets/css/style.css';

@Component({
  components: {HeaderContainer}
})
export default class Index extends Vue {

}
</script>
