<template>
  <div id="app">
    <tool-bar></tool-bar>
    <transition name="page">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import ToolBar from './components/ToolBar';

export default {
  components: {
    toolBar: ToolBar,
  },

  methods: {
    fetchData() {
      console.log('hello');
    }
  }
}

</script>

<style>
body {
  padding: 0;
  margin: 0;
}

/* router transition */
.page-enter-active, .page-leave-active {
  transition: opacity .5s;
}
.page-enter, .page-leave-to {
  opacity: 0;
}

a {
  text-decoration: none;
}
a.router-link-exact-active {
  text-decoration: underline;
}
a:hover {
  color: #42B883;
  text-decoration: underline;
} 

</style>
