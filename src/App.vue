<template>
  <transition name="fade">
    <router-view/>
  </transition>
</template>

<style lang="scss">

// { id: 9, image: 'tricerax.png', title: "Трицератопс", subTitle: "", firstText: "", secondText: ""}
#app {
  font-family: Open Sans, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
  opacity: 0;
}
</style>
