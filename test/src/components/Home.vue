<template>
  <div>Hola</div>
</template>

<script>
import { onMounted } from "vue";
export default {
  name: "HomeComponent",
  setup() {
    onMounted(()=>{
      console.log("mounted!");
    });
  },
};
</script>
