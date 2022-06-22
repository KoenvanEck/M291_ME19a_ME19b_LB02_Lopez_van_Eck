<template>
  <!-- Vue Directives: (v-text, v-once, v-html, v-bind, v-if, v-show) -->
  <div>
    <h1 v-if="false" v-text="text">Loading...</h1>
    <h2 v-else-if="false" v-html="html" />
    <a
      v-else
      :href="link.url"
      :target="link.target"
      :tabindex="link.tabindex"
      v-text="link.title"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      // v-text
      text: 'Tell us your favourite artists and their top 3 songs',
      // v-html
      html: 'The Link </br>is shortened<br/><b>but its legit</b>',
      // v-bind
      link: {
        url: 'https://tinyurl.com/whnbm2wa',
        target: '_blank',
        tabindex: '0',
        title: 'Take the survey here',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
h1 {
  color: #00b4d8;
}

h2 {
  margin: 4rem 0 0;
  font-weight: normal;
  color: #e63946;
}

a {
  display: block;
  margin-top: 4rem;
}
</style>
