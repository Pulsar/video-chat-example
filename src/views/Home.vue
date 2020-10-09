<template>
  <div class="home">
    <h1>Home</h1>
    <p>Welcome {{ user }}</p>
  </div>
</template>
<script>
import db from '../db.js'
export default {
  name: 'home',
  data: function() {
    return {
      user: null
    }
  },
  mounted() {
    db.collection('users')
      .doc('jUOHf2Mcci2pWDZBASYO')
      .get()
      .then(snapshot => {
        this.user = snapshot.data().name
      })
  }
}
</script>
