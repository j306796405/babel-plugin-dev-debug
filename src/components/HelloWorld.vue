<template>
  <div class="hello">
    <button @click="handleClick">click</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: String
  },
  setup () {
    const handleClick = () => {
      console.log('click1')
      if (DEBUG) {
        console.log('for debug')
        const a = 10
        const b = 20
        console.log(a + b)
      }
    }

    return {
      handleClick
    }
  }
})
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
