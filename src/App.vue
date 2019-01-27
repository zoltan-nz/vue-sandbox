<template>
  <div id="app" v-on:mousemove="mousePosition">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>

    <div draggable="true" v-on:dra>
      My Stuff
    </div>
    <router-view />
  </div>
</template>

<script lang="ts">
  export default {
    methods: {
      mousePosition(event: MouseEvent) {
        console.log(event.clientX, event.clientY);
      }
    }
  }
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
