<template>
  <div id="app">
    <sandbox hide-help v-slot="config">
      <v-select v-bind="config" :grouped="true" group-label="myLabel" group-list="myList" label="title" @open="open" @close="close" />
    </sandbox>
  </div>
</template>

<script>
import vSelect from '../src/components/Select';
import Sandbox from '../docs/.vuepress/components/Sandbox';
// import countries from '../docs/.vuepress/data/countryCodes';
// import books from '../docs/.vuepress/data/books';

export default {
  components: {Sandbox, vSelect},
  methods: {
	  open() {
		console.log('open');
	  },
	  close() {
		console.log('close');
	  }
  }
};
</script>

<style>
  html,
  body {
    margin: 0;
    height: 100%;
    font-family: -apple-system, sans-serif;
  }

  #app {
    height: 100%;
  }

  hr {
    border: none;
    border-bottom: 1px solid #cacaca;
    margin-bottom: 1em;
    padding-top: 1em;
    width: 90%;
  }
</style>
