<template>
  <div>
    <h1 class="" v-on:click="changeHeader">{{ headerSub }}</h1>
  </div>
</template>

<script>
import { bus } from '../main'
export default {
  name: 'Test',
  props: {
    header: {
      type: String
    }
  },
  data (){
    return {
      headerSub: 'pippo1'
    }
  },
  methods: {
    changeHeader (){
      // eslint-disable-next-line
      console.log('bottom2--------------------------', this.headerSub);
      //this.headerSub = "changed header";
      bus.$emit('changeIt', this.headerSub);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
