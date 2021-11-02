<script setup lang="ts">
import { ref, onMounted } from 'vue'
import HelloWorld from './HelloWorld.vue'

const searchRef = ref<HTMLElement>()
onMounted(() => { searchRef.value?.focus() })

const helloRef = ref<InstanceType<typeof HelloWorld>>()
onMounted(() => { helloRef.value?.msg })
</script>

<template>
  <input type="search" ref="searchRef">
  <HelloWorld ref="helloRef" msg="hello world" />
</template>