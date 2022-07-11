<template>
  <div>{{fullName}}</div>
  <div>{{username}}</div>
  <button ref="btn">Click!</button>
</template>

<script>
  export default {
    name: "HomeComponent"
  }
</script>
<script setup>
import { defineExpose, defineProps, watch, ref, toRefs, computed, inject } from "vue" 
  const props = defineProps({
    firstName: String,
    lastName: String,
  })
  
  
    const {firstName, lastName} = toRefs(props);

    const fullName = computed(()=>{
      return `${firstName.value} ${lastName.value}`;
    });

    const username = inject("username");

    defineExpose({
      fullName
    });

    const btn = ref(null)

    console.log(btn.value);

    watch(btn, (valor)=>{
      console.log(valor)
    });

</script>
