<template>
  <header id="header">
    <div class="inner">
      <a href="#" class="logo">LOGO</a>
      <MainGnb/>
      <div class="user_menu_container">
        <div>회원가입</div>
        <div class="write_btn">글쓰기</div>
      </div>
    </div>
  </header>
</template>

<script>
import {Component, Vue} from 'vue-property-decorator'
import MainGnb from "~/components/header/mainGnb.vue";

@Component({
  components: { MainGnb }
})
export default class HeaderContainer extends Vue {
}
</script>
