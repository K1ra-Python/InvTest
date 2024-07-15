<template>
  <div>
    <greenObject></greenObject>
    <blueObject></blueObject>
    <yellowObject></yellowObject>
    <div class="row1">
        <div class="cell1"></div>
    </div>
    <div class="row2"></div>
    <div class="row3"></div>
    <div class="row4"></div>
    <div class="row5"></div>
  </div>
</template>

<script setup>
import draggableComponent from 'vuedraggable';
import greenObject from './insideInventory/greenObject.vue';
import yellowObject from './insideInventory/yellowObject.vue';
import blueObject from './insideInventory/blueObject.vue';


</script>

<style lang="scss">

</style>