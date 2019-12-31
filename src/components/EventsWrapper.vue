<template>
  <div class="events">
    <p>Events</p>
    <div id="v-for-object" class="demo">
        <div v-for="data in myJson" v-bind:key="data">
            <Event :msg="data.title"/>            
        </div>
    </div>
  </div>
</template>

<script>
import Event from './Event.vue'
import lines from '../json/lines.json'
export default {
  name: 'EventsWrapper',
  components: {
      Event
  },
  props: {
    msg: String
  },
    data() {
        return {
            myJson: lines
        }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.events {
    background-color: #333;
    padding: 1em;
}
.demo {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

</style>
