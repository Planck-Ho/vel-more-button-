<template>

  <div id="resizable">
    <VelMoreButtonGroup>
      <VelMoreButtonItem content="Button1" @click="callback" />
      <VelMoreButtonItem content="Button2" type="primary">
        <VelMoreButtonItem content="Button2-1" @click="callback" />
        <VelMoreButtonItem content="Button2-2">
          <VelMoreButtonItem content="Button2-2-1" @click="callback" />
          <VelMoreButtonItem content="Button2-2-2" @click="callback" />
        </VelMoreButtonItem>
        <VelMoreButtonItem content="Button2-3" @click="callback" />
      </VelMoreButtonItem>
      <VelMoreButtonItem content="Button3" type="success" @click="callback"></VelMoreButtonItem>
      <VelMoreButtonItem content="Button4" type="info" @click="callback"></VelMoreButtonItem>
      <VelMoreButtonItem content="Button5" type="warning" @click="callback"></VelMoreButtonItem>
      <VelMoreButtonItem content="Button6" type="danger" @click="callback"></VelMoreButtonItem>
    </VelMoreButtonGroup>
  </div>

</template>

<script setup lang="ts">
import { VelMoreButtonGroup, VelMoreButtonItem } from './components'

const callback = (e: Event) => {
  console.log('callback', e)
}
</script>
<style>
#resizable {
  padding: 50px;
  width: 25vw;
  height: 150px;
  border: 1px solid black;
  position: relative;
  resize: both;
  overflow: auto;
}
</style>