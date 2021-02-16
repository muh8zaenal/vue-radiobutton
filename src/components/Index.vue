<template>
  <div>
    <div class="box">
      <h3>1. Passing label with props</h3>
      <radio-button value="1" label="Button A" v-model="radio1"/>
      <radio-button value="2" label="Button B" v-model="radio1"/>
    </div>
    <div class="box">
      <h3>2. Add subcomponent</h3>
      <radio-button value="2" label="Inner Component" v-model="radio2">
        <template v-slot:subcomponent>
          <input v-model="message" placeholder="Hey!" >
        </template>
      </radio-button>
      <br>
      <radio-button value="3" label="Representative Form" v-model="radio2">
        <template v-slot:subcomponent>
          <subfield/>
        </template>
      </radio-button>
    </div>
  </div>
</template>

<script>
import RadioButton from './RadioButton.vue'
import Subfield from './Subfield.vue'

export default {
  components:{
    RadioButton,
    Subfield,
  },
  data(){
    return{
      radio1: '',
      radio2: '',
      message: '',
      Subfield: this.Subfield,
    }
  },
}
</script>

<style scoped>
.box 
{
  width: 500px;
  border: 1pt rgb(61, 60, 60) solid;
  border-radius: 3px;
  margin: 10px auto;
  text-align: start;
  padding-left: 10px;
  overflow: auto;
  color: rgb(96, 70, 70);
}
</style>