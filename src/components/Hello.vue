<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ text }}</h2>
    <ul>
      <li v-for="item in lists">
        <a v-bind:href="item.link" target="_blank">{{ item.info }}</a>
      </li>
    </ul>
    <h2>hi～{{ seen ? '强哥' : 'jartto'}}
    <button v-on:click="reverseMessage">切换</button>
    <div>
      <input v-model="text">
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      text: 'Hello World!',
      seen: true,
      lists: [{ info: 'Core Docs', link: 'https://vuejs.org' },
        { info: 'Forum', link: 'https://forum.vuejs.org' },
        { info: 'Gitter Chat', link: 'https://gitter.im/vuejs/vue' }
      ]
    }
  },
  methods: {
    reverseMessage () {
      this.seen = !this.seen
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
