<template>
  <div><Modal /></div>
  <button @click="show = !show">Menu</button>
  <transition name="fade">
    <Menu v-show="show" />
  </transition>
</template>

<script>
import Modal from "./components/Modal";
import Menu from "./components/Menu";

export default {
  name: "App",
  components: { Menu, Modal },
  data() {
    return {
      show: false,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.fade-enter-from {
  opacity: 0;
}
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active,
.fade-enter-active {
  transition: opacity 0.5s ease;
}
</style>
