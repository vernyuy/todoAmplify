<template>
  <div>
    <div>
      <Nav />
    </div>
    <router-view />
  </div>
</template>
<script>
import Nav from "./components/Nav.vue";
import { mapActions } from "vuex";
export default {
  mounted() {
    this.authAction();
  },
  components: {
    Nav,
  },
  methods: {
    ...mapActions("auth", ["authAction"]),
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
}
#nav {
  padding: 30px;
  /* {
    font-weight: bold;
    color: #2c3e50;
    router-link-exact-active {
      color: #42b983;
    }
  } */
}
</style>