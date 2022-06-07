<template>
  
  <div class="hello">
  <div>{{text}}</div>
    <input type="text" v-model="input" @keyup="test">
   <div> {{input}}</div>
  </div>

</template>


<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      input: "",
      text: `It was going to rain. The weather forecast didn't say that, but the steel plate in his hip did. He had learned over the years to trust his hip over the weatherman. It was going to rain, so he better get outside and prepare.`
    }
  },
  methods: {
    test () {
      let inputArray = this.input.split('')
      let textArray = this.text.split('')
      for (let i = 0; i < textArray.length; i++) {
        if (inputArray[textArray.length - i] === textArray[textArray.length - i]){
          let woo = "woo"
          woo + "sdf"
        }else {
          console.log("incorrect", textArray.length - i)
        }
      }
      // console.log(textArray)
      // console.log(inputArray)
    }
  }
}
</script>

<style scoped>
.hello {
  display: block;
}
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
