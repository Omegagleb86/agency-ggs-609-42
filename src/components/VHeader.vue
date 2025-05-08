<script setup>

</script>

<template>
  <header>
    <nav class="desktop-navigation">
      <div class="container">
        <div class="desktop-navigation__wrap">
          <img src="@/assets/img/logo.png" alt="" class="logo">
          <ul class="navigation__list">
            <li class="navigation__list-element_active"><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Sevices</a></li>
            <li><a href="#">Projects</a></li>
          </ul>
          <button class="button-primary">
            Contact us
          </button>
        </div>
      </div>
    </nav>
    <nav class="mobile-navigation">
      <div class="mobile-navigation__wrap">
        <div class="mobile-navigation__header">
          <img src="@/assets/img/logo-mobile_navigation.png" alt="Agency" class="desktop-navigation__logo" />
          <button class="mobile-navigation__header-button">
            <img src="@/assets/img/menu-open.svg" alt="" class="icon_menu-open">
            <img src="@/assets/img/menu-close.svg" alt="" class="icon_menu-close">
          </button>
        </div>
        <div class="mobile-navigation__content">
          <ul class="navigation__list">
            <li class="desktop-navigation__list-element_active">
              <a href="#">Home</a>
            </li>
            <li>
              <a href="#">About</a>
            </li>
            <li>
              <a href="#">Services</a>
            </li>
            <li>
              <a href="#">Projects</a>
            </li>
          </ul>
          <div class="navigation__buttons">
            <button class="button-primary">Contact us</button>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped>

</style>
