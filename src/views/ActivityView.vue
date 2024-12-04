<template>
    <div>
        <p>This is a template</p>
        <span>Message: {{ msg }}</span>
        <p>This is the html message: <span v-bind:id="`color-${colorSuffix}`" v-html="msg"></span> </p>
        <button v-on:click="toggleColor">Change Text Color</button>
    </div>
</template>
<script setup lang="ts">
import { ref } from 'vue';

const msg = '<h3>Welcome<h3/>';
const colorSuffix = ref('red');

function toggleColor() {
    colorSuffix.value = colorSuffix.value === 'red' ? 'blue' : 'red';
}

</script>
<style lang="css">
#color-red {
    color: red;
}

#color-blue {
    color: blue
}
</style>