<script setup lang="ts">
import GUI from 'lil-gui'
import { useConfig } from '../store/config'
import { useBeforeMount } from '../utils/index'

const config = useConfig()
const gui = new GUI()
useBeforeMount(() => {
  const envLight = gui.addFolder('light')
  envLight.add(config, 'envWeight', 0, 1)
  envLight.add(config, 'envIntensity', 0, 1)

  const car = gui.addFolder('car')
  car.addColor(config, 'carColor')

  const action = gui.addFolder('action')
  action.add(config, 'showSpeedUp')

  action.add(config, 'showCurvature')

  // const test = gui.addFolder('test')
  // test.add(state, 'strength', 0, 1)
  // test.add(state, 'radius', 0, 1)
  // test.add(state, 'threshold', 0, 1)

  return () => {
    envLight.destroy()
  }
})
</script>
<template></template>
