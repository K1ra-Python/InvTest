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
  <draggable class="list-group" v-model="meals" tag="div">
    <template #item="{ element: meal }">
      <div class="block">{{ meal.name }}</div>
    </template>
  </draggable>

</template>

<script setup>
import draggable from 'vuedraggable'
import greenObject from './insideInventory/greenObject.vue'
import yellowObject from './insideInventory/yellowObject.vue'
import blueObject from './insideInventory/blueObject.vue'
import { ref } from 'vue'

const 

const items = {

};

const meals = ref([
  { name: 'Joao', id: 2 },
  { name: 'empty', id: 0 },
  { name: 'empty', id: 0 },
  { name: 'empty', id: 0 },
  { name: 'Jean', id: 3 },
  { name: 'empty', id: 0 },
  { name: 'John', id: 1 },
  { name: 'empty', id: 0 },
  { name: 'empty', id: 0 }
])

</script>

<style lang="scss">
.block {
  width: 100px;
  height: 100px;
}
.list-group {
  display: flex;
  flex-wrap: wrap;
}
</style>
