<template>
  <div class="header">
    <p class="title">Brightness & Contrast</p>
    <p class="subtitle">Developer Test</p>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    title: String,
    subtitle: String
  }
}
</script>

<style scoped lang="scss">
.header {
    background-color: #7344C0;
    padding-top: 1em;
    padding-bottom: 1em;
}

.title, .subtitle {
    color: white;
}

.title {
  font-size: 0.96em;
  font-weight: 600;
  //font-family: 'Graphik-Medium';
}

.subtitle {
  margin-top: 0.3em;
  font-size: 0.8em;
  //font-family: 'Graphik-Regular';
}
</style>
