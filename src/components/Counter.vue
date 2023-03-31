<script setup lang="ts">
import { ref } from 'vue'
const counter = ref(0)

function handleCounter (isDecreasing: boolean) {
    if (isDecreasing) return counter.value -= 1
    counter.value += 1
}
</script>

<template>
    <div>
        <h3>Counter: {{ counter }}</h3>
        <button class="button" @click="handleCounter(false)">Increase</button>
        <button class="button" @click="handleCounter(true)">Decrease</button>
    </div>
</template>

