<template>
  <div class="router2">
    <!--<load-js :src="../assets/js/toggle.js"></load-js>-->
    <div class="js-toggle" @click="clickDiv">
      {{msg}}
    </div>
    <router-link :to="{name: 'HelloWorld'}" class="nav-link" active-class="active">HelloWorld</router-link>
  </div>
</template>

<script>
import '../assets/js/toggle.js'

export default {
  name: 'router2',
  data () {
    return {
      msg: 'router2'
    }
  },
  methods:{
    clickDiv (){
      console.log('click div')
    }
  },
  components: {
/*    'load-js':{
      render(createElement) {
        return createElement('script', { attrs: { type: 'text/javascript', src: this.src}})
      },
      props: {
        src: { type: String, required: true},
      }
    }*/
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
