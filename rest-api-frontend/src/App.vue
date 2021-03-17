<template>
  <div id="app">
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'App',
  components: {
  },
  data () {
    return {
      arrClassroom: []
    }
  },
  async created() {
    try{
      const { data } = await axios.get("http://localhost:1234/get-students");
      // data.forEach(student => {
        // console.log(this.arrClassroom);
        // this.arrClassroom[student.classroom]++;
      // });
      console.log(data);
    } catch(err){
      console.error(err);
    }
  }
}
</script>

<style>

</style>