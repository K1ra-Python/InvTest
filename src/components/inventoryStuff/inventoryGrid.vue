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
        <button  @click="showDisplay(it.name, it.quantity, it.color)" v-if="it.name != null">Показать описание</button>
        {{ it.name }}
        {{ it.quantity }}
      </div>
    </template>
  </draggable>
  <div class="display" v-if="isShow == true">
    {{ nm }}
    {{ qt }}
    {{ clr }}
    <button @click="deleteObj(qt)">Удалить объект</button>
  </div>
</template>

<script setup>
import draggable from 'vuedraggable'

import { ref } from 'vue'
const isShow = ref(false);
const nm = ref();
const qt = ref();
const clr = ref();
const items = ref([
  {
    name: 'Зелёный блок',
    color: 'green',
    quantity: ref(10)
  },
  {
    name: 'Жёлтый блок',
    color: 'yellow',
    quantity: ref(10)
  },
  {
    name: 'Синий блок',
    color: 'blue',
    quantity: ref(10)
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


function showDisplay(name,quantity, color) {
  if (isShow.value === false) {
    isShow.value = true;
  
  }
  nm.value = name;
  qt.value = quantity;
  clr.value = color;
  
}

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

.display{
  border-left: 1px solid #4d4d4d;
width: 250px;
height: 500px;
backdrop-filter: blur(16px);
background: rgba(38, 38, 38, 0.5);
}
</style>
