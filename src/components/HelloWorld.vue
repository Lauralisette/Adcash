<template>
  <div v-for='(tag, index) in tags' :key='tag' class='tag-input__tag'>
    {{ tag }}
      <span @click='removeTag(index)'>Remove</span> |
      <span @click='editTag(index)'>Edit</span>
      
      </div>
  <div class='tag-input' >
    <input 
      type='number' 
      placeholder="Enter a Tag" 
      class='tag-input__text' 
      @keydown.enter='addTag' 
      @keydown.space='addTag'
/>
  </div>

</template>
<script>
export default {
  data () {
    return {
      tags: []
    }
  },
  methods: {
    addTag (event) {
      event.preventDefault()
      var val = event.target.value.trim()
      if (val.length > 0) {
        this.tags.push(val)
        event.target.value = ''
      }
},
removeTag (index) {
      this.tags.splice(index, 1)
},
editTag(index){
  this.tags.splice(index,1)
}

}
};
</script>
<style scoped>
.tag-input {
  width: 95%;
  font-size: 0.9em;
  height: 50px;
  box-sizing: border-box;
  padding: 0 10px;
  margin: 0 auto;
  
}

input{
  float:left;
}
div{
  font-family:'Trebuchet MS', sans-serif;
}

.tag-input__tag {
  height: 30px;
  float: left;
  margin-left: 30px;
  margin-right: 30px;
  background-color: #eee;
  opacity: 0.9;
  margin-top: 10px;
  line-height: 30px;
  padding: 0 5px;
  border-radius: 5px;
  
}

.tag-input__tag > span {
  cursor: pointer;
  opacity: 0.3;
  margin: 0 auto;
}

.tag-input__text {
  border: none;
  outline: none;
  font-size: 0.9em;
  line-height: 50px;
  background: none;
  margin: 0 auto;
  
}
::placeholder {
  color: white;
  opacity:0.4;
}
</style>