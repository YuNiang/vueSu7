<script setup lang="ts">
import { useBeforeMount } from '../utils/index'
import { getThreeEnv } from '../store/three'
// import { destroyObject3D } from '../lib/three-common'
const env = getThreeEnv()

useBeforeMount(() => {
})
</script>
<template>
  <slot />
</template>
