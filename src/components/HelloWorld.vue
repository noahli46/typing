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
      text: `Housework could be everyone’s work, not just “women’s work”.
       Why do women enable men to act oblivious to cleaning, grocery shopping, pet feeding, etc? 
       Somehow when men live alone they figure out how to do all of those things all on their own. 
       My friend’s husband claimed he didn’t know that sheets should be washed more than once a season.
        He said he didn’t know one had to clean toilets. He assumed that since you flush toilets they clean themselves.
         She tried to get him to help but he did an awful job so she let him off the hook.
          Wouldn’t it be better if she spent the time and energy to get him to do it right instead of letting him claim he is “just bad at it”.
           My sons were raised to clean toilets and change their own sheets. Hopefully, in their future homes, the housework will be equally divided.`
    }
  },
  methods: {
    test () {
      let inputArray = this.input.split('')
      let textArray = this.text.split('')
      
      for (let i = 0; i < inputArray.length; i++) {
        if (inputArray[i] === textArray[i]){
          console.log(i,"yep")
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
