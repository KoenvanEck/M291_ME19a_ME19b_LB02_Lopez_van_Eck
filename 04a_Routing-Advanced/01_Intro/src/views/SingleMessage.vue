<template>
  <div>
    <h1>Einzelne Nachricht</h1>
    {{$route.params.content}}
  </div>
</template>

<script>
export default {
  name: "SingleMessage"
}
</script>
