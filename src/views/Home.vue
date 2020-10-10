<template>
  <div class="home">
    <h1>Home</h1>
    <p>Welcome {{ user }}</p>
  </div>
</template>
<script>
export default {
  name: 'Home',
  props: ['user']
}
</script>
