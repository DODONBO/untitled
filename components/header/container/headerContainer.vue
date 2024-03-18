<template>
  <header id="header">
    <div class="inner">
      <a href="#" class="logo">LOGO</a>
      <MainGnb/>
      <div class="user_menu_wrap">
        <div class="search_wrap">
          <div class="search_icon" @click="toggleSearchWrap($event)">
            <font-awesome-icon :icon="['fas', 'magnifying-glass']" />
          </div>
          <div class="search_input">
            <input type="text">
          </div>
          <div class="search_close_btn" @click="minimizeSearchWrap()">
            <font-awesome-icon :icon="['fas', 'xmark']" />
          </div>
        </div>
        <div class="user_menu_container">
          <div class="sign_in_btn btn">회원가입</div>
          <div class="write_btn btn">글쓰기</div>
        </div>
      </div>
    </div>
  </header>
</template>
<script lang="ts">
import {Component, Vue} from 'vue-property-decorator'
import MainGnb from "~/components/header/mainGnb.vue";
import $ from 'jquery';

@Component({
  components: { MainGnb }
})
export default class HeaderContainer extends Vue {

  private toggleSearchWrap(e: Event): void {
    const $currentTargetParent: JQuery<EventTarget> = $(e.currentTarget!).parent('.search_wrap');

    if ($currentTargetParent.hasClass('on')) {
      $currentTargetParent.removeClass('on');

    } else {
      $currentTargetParent.addClass('on');
    }
  }

  private minimizeSearchWrap(): void {
    $('.search_wrap').removeClass('on');
  }

}
</script>
