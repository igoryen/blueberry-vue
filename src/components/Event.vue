<template>
  <div class="event">
    <p>I am one event</p>
    <div id="v-for-object" class="demo">
        <div v-for="name in person" v-bind:key="name">
            <Row :msg="name"/>
            
        </div>
    </div>
  </div>
</template>

<script>
import Row from './Row.vue'
export default {
  name: 'Event',
  components: {
      Row
  },
  props: {
    msg: String
  },
    data() {
        return {
            person: {
                firstName: 'Igor',
                lastName: 'Yen',
                gender: 'male'
            }
        }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.event {
    background-color: #333;
    padding: 1em;
}
.demo {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

</style>
