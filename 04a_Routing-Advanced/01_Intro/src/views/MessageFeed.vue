<template>
  <div>
    <h1>Feed</h1>
    <div v-for="(m, i) in messages" :key="i" >
      <router-link :to="{ name: 'singlemessage', params: {content: m}}">
        {{ m }}
      </router-link>
    </div>
</div>
</template>
<script>
export default {
  data() {
    return {
      messages: [
        'Hello, have you listened to OBNs new song yet?',
        'What is your opinion on Michael Jackson?',
        'Did you ever get rickrolled?',
        'My favourite genre is rnb, what is yours?'
      ]
    }
  }
}
</script>
