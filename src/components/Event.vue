<template>
  <div class="event">
    <p>I am one event</p>
    <ul id="v-for-object" class="demo">
        <li v-for="(value, name) in person" v-bind:key="(value,name)">
            {{ name }}: {{ value }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Event',
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
