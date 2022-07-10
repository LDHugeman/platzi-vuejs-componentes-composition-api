<template>
  <div>{{fullName}}</div>
</template>

<script>
import { toRefs, computed } from "vue" 
export default {
  props: {
    firstName: String,
    lastName: String,
  },
  name: "HomeComponent",
  
  setup(props) {
    const {firstName, lastName} = toRefs(props);

    const fullName = computed(()=>{
      return `${firstName.value} ${lastName.value}`;
    })

    return{
      fullName
    }
  },
};
</script>
