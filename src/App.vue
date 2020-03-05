<template>
  <body>
    <h1>🦊 Vue Vixens Mad Libs 🦊</h1>
    <br />
    <button @click="toggleCensored">toggle censoring</button>
    <div>
      <p v-if="censored" class="censored">
        A brief history of the 
        <label for="adjective-1">Adjective</label>
        <input id="adjective-1" v-model="input1" placeholder="<adjective>"/>
        state of Texas. Texas was founded as a state in 
        <label for="adjective-1">Adjective</label>
        <input v-model="input2" placeholder="<year>"/>. It is known for 
        <label for="adjective-1">Adjective</label>
          <input v-model="input3" placeholder="<activity>"/>, 
        <label for="adjective-1">Adjective</label>
            <input v-model="input4" placeholder="<adjective>"/> 
              foxes that roam about, and generally
        <label for="adjective-1">Adjective</label>
               <input v-model="input5" placeholder="<adjective>"/> 
                 weather. Hah, hah, that was totally 
        <label for="adjective-1">Adjective</label>
                 <input v-model="input6" placeholder="<boolean>" />! Anyway, I am 
        <label for="adjective-1">Adjective</label>
                   <input v-model="input7" placeholder="<emotion>" />
                     to learn some TypeScript today! What's your name?</p>
     
      <p v-if="!censored" class="revealed">
        A brief history of the 
        <label for="adjective-1">Adjective</label>
        <input id="adjective-1" v-model="input1" placeholder="<adjective>"/>
        state of Texas. Texas was founded as a state in 
        <label for="year-2">Adjective</label>
        <input id="year-2" v-model="input2" placeholder="<year>"/>. It is known for 
        <label for="adjective-2">Adjective</label>
          <input id="adjective-2" v-model="input3" placeholder="<activity>"/>, 
        <label for="adjective-3">Adjective</label>
            <input id="adjective-3" v-model="input4" placeholder="<adjective>"/> 
              foxes that roam about, and generally
        <label for="adjective-4">Adjective</label>
               <input id="adjective-4" v-model="input5" placeholder="<adjective>"/> 
                 weather. Hah, hah, that was totally 
        <label for="adjective-1">Adjective</label>
                 <input v-model="input6" placeholder="<boolean>" />! Anyway, I am 
        <label for="adjective-1">Adjective</label>
                   <input v-model="input7" placeholder="<emotion>" />
                     to learn some TypeScript today! What's your name?</p>
     
                   </div>
  </body>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    const censored = ref(true);
    const count = ref(0);
    const toggleCensored = () => {
      censored.value = !censored.value;
    }
    const input1 = ref('');
    const input2 = ref('');
    const input3 = ref('');
    const input4 = ref('');
    const input5 = ref('');
    const input6 = ref('');
    const input7 = ref('');
    return {
      input1,
      input2,
      input3,
      input4,
      input5,
      input6,
      input7,
      count,
      censored,
      toggleCensored,
    };
  },
  methods: {

  },
})  
</script>

<style>
body {
  font-family: Gill Sans;
  background-color:rgb(65, 143, 146);
}
input {
  background-color:rgb(200, 255, 0);
  border: 3px solid black;
  color: black;
  font-family: Gill Sans;
  font-size: 1em;
  width: 200px;
  resize: horizontal;
}
label {
  position: absolute;
  height: 1px;
  width: 1px;
  overflow: hidden;
  text-overflow: clip;
  visibility: hidden;
  white-space: nowrap;
  clip: rect(1px 1px 1px 1px); /* IE6, IE7 */
  clip: rect(1px, 1px, 1px, 1px);
}
h1 {
  font-size: 4em;
  font-family: monospace;
  text-align: center;
}
p {
  font-size: 2.5em;
}
.censored {
  background-color: black;
}
.revealed {
  background-color: 'transparent';
}
button {
  width: 200px;
  font-size: 2em;
  font-family: Gill Sans;
}
</style>
