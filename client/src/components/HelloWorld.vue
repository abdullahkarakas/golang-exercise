<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul v-for="link in links" v-bind:key="link">
      <li>
        <a :href="link.src" target="_blank" rel="noopener">{{ link.text }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      links: [
        {
          text: "Core Docs",
          src: "https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel",
        },
        {
          text: "Forum",
          src: "https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint",
        },
        { text: "Community Chat", src: "https://vuejs.org" },
        { text: "Twitter", src: "https://forum.vuejs.org" },
        { text: "News", src: "https://chat.vuejs.org" },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
