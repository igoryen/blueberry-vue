<template>
  <div class="event">
    <p>I am one event</p>
  </div>
</template>

<script>
export default {
  name: 'Event',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.event {
    background-color: #333;
    padding: 1em;
}

</style>
