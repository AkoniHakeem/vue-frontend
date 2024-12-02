<template>
  <div>
    <h1>This is an about page</h1>
    <br>
    <div>
      <h2>Hmn, this is looking great!</h2>
    </div>
    <div>
      <div>
        <button style="font-size: larger;" @click="increment">Click Me , and Watch( {{ count }} )</button>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'
const count = ref(0);
function increment() {
  count.value++;

}
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
