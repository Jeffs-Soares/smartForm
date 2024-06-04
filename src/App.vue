<template>
  <div class="grid justify-center pt-10 bg-gradient-to-r from-gray-100 to-blue-400 h-screen">
      <div class="slide">

        <div id="1">

          <h1> Qual seu nome?</h1>

            <input v-model="dados.q1"  >

        </div>

        <div id="2" hidden>

          <h1> Qual seu whats?</h1>

          <input v-model="dados.q2"  >

        </div>


        <h1 id="3" hidden> Button pra mandar os dados pra api </h1>

      </div>

      <div class="button">

        <button @click="next" > Next >> </button>

      </div>
  </div>
</template>

<script setup>

import {reactive, ref} from "vue";

const dados = reactive([{
  q1: '',
  q2: ''
}])


const isActive = ref(1);

function next() {

  const array = document.querySelector('.slide').childNodes;
  const index = isActive.value;

  const button = document.querySelector('.button').childNodes;



  if (isActive.value === Number(array[index - 1].id)) {

    array[index - 1].hidden = 'true';

    isActive.value++;

    array[index].hidden = '';
  }

  if (isActive.value > 2) {
    button[0].hidden = 'true';
  }

}

</script>