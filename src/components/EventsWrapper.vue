<template>
  <div class="events">
    <p>Events</p>
    <div class="form-group">
        <label>Username</label>
        <input type="text" class="form-control" v-model="user.username">
    </div>
    <div class="form-group">
        <label>Mail</label>
        <input type="text" class="form-control" v-model="user.email">
    </div>
    <button @click="submit">Submit</button>
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
            user: {
                username: '',
                email: ''
            },
            myJson: lines
        }
    },
    methods: {
        submit() {
            this.$http.post('https://blueberry-f0510.firebaseio.com/data.json', this.user)
            .then( 
                response => { console.log(response); },
                error => { console.log(error); }
            );
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
