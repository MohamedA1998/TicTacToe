<script>
import { computed, reactive, ref } from 'vue';
import Board from './components/Board.vue';

const START_FROM = 25;
export default {
  components: { Board },

  setup() {
    const counter = ref(5);

    const multiplied = computed(
      () => counter.value * 10
    )

    const x2 = computed(
      () => multiplied.value * counter.value
    )

    const xxx = reactive({ count: 10 })

    const ra = ref([1, 2, 3])

    const repaceArray = () => ra.value = [4, 5, 6]

    const increase = () => counter.value++

    return { x2, ra, repaceArray, xxx, counter, multiplied, increase, START_FROM }
  }
}
</script>

<template>
  <Board />

  <!-- <h1>Mohamed Alsayed {{ counter }}</h1>
  <button @click="increase">increase</button>

  <button @click="repaceArray">Replace</button>

  <p>{{ xxx.count }}</p>

  <h1>{{ ra }}</h1> -->
</template>