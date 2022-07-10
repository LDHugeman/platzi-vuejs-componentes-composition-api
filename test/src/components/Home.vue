<template>
  <div>{{obj}}</div>
</template>

<script>
import { ref } from "vue" 
export default {
  name: "HomeComponent",
  setup() {
    const obj = ref({counter: 0});
    
    setInterval(()=> obj.value.counter++, 500);

    return{
      obj,
    }
  },
};
</script>
