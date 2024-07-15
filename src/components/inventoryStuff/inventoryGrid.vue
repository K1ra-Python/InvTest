<template>
  <div>
    <div class="row1">
      <div class="cell1"></div>
    </div>
    <div class="row2"></div>
    <div class="row3"></div>
    <div class="row4"></div>
    <div class="row5"></div>
  </div>
  <draggable class="list-group" v-model="items" tag="div">
    <template #item="{ element: it }">
      <div class="block">
        {{ it.name }}
        {{ it.quantity }}
      </div>
    </template>
  </draggable>
</template>

<script setup>
import draggable from 'vuedraggable'

import { ref } from 'vue'

const items = ref([
  {
    name: 'Зелёный блок',
    color: 'green',
    quantity: ref(1)
  },
  {
    name: 'Жёлтый блок',
    color: 'yellow',
    quantity: ref(1)
  },
  {
    name: 'Синий блок',
    color: 'blue',
    quantity: ref(1)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
  { name: null, 
    color: null, 
    quantity: ref(null)
  },
])
</script>

<style lang="scss">
.block {
  width: 100px;
  height: 100px;
  border: 3px solid black;
}
.list-group {
  width: 700px;
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
}
</style>
