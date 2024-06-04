<template>
  <div class="grid justify-center pt-10 bg-gradient-to-r from-gray-100 to-blue-400 h-screen">
      <div class="slide">

        <div id="1">
          <h1> Qual seu nome?</h1>
            <input v-model="dados.q1"  >
        </div>

        <div id="2" hidden>
          <h1> Qual seu whats?</h1>
          <input v-model="dados.q2">
        </div>

        <div id="3" hidden>

          <h1> Qual seu site? </h1>
          <span class="block text-[10px] opacity-45 mb-2"> Se não possuir, deixe em branco...</span>

          <input v-model="dados.q3">

        </div>

        <div id="4" hidden>

          <h1> Qual seu instagram? </h1>
          <input v-model="dados.q4">

        </div>

        <div id="5" hidden>

          <h1> Seu negócio fatura mais de R$ 15.000 por mês? </h1>

          <input type="radio"  value="sim" v-model="dados.q5" />
          <label for="one"> Sim </label>

          <input type="radio"  value="nao" v-model="dados.q5" />
          <label for="two"> Não </label>

        </div>

        <div id="6" hidden>

          <h1> Qual a média de faturamento mensal do seu negócio ? </h1>

          <div class="flex flex-col items-start">

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="A" v-model="dados.q6" />
              <label for="A"> Entre R$ 15.000 a R$ 30.OOO </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="B" v-model="dados.q6" />
              <label for="B"> Entre R$ 30.000 a R$ 50.OOO </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="C" v-model="dados.q6" />
              <label for="C"> Entre R$ 50.000 a R$ 100.OOO </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="D" v-model="dados.q6" />
              <label for="D"> Acima de R$ 100.000 </label>
            </div>
          </div>

        </div>

        <div id="7" hidden>

          <h1> Quanto investe mensalmente em tráfego pago?  </h1>

          <div class="grid items-center">

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="A" v-model="dados.q7" />
              <label for="A"> Não invisto ainda. </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="B" v-model="dados.q7" />
              <label for="B"> Entre R$ 500 A R$1.000  </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="C" v-model="dados.q7" />
              <label for="C"> Entre R$ 2.000 a R$ 5.000 </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="D" v-model="dados.q7" />
              <label for="D"> Entre R$ 5.000 a R$ 10.000  </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="E" v-model="dados.q7" />
              <label for="E"> Acima de R$ 10.000 </label>
            </div>
          </div>
        </div>


        <div id="8" hidden>

          <h1> Há quanto tempo sua marca está no mercado?  </h1>

          <div class="grid items-center">

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="A" v-model="dados.q8" />
              <label for="A"> Menos de 1 ano </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="B" v-model="dados.q8" />
              <label for="B"> Entre 1 a 2 anos  </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="C" v-model="dados.q8" />
              <label for="C"> Entre 2 a 3 anos </label>
            </div>

            <div class="flex items-center gap-2 justify-center">
              <input type="radio"  value="D" v-model="dados.q8" />
              <label for="D"> Mais de 3 anos   </label>
            </div>

          </div>


        </div>


        <h1 id="7" hidden> Button pra mandar os dados pra api </h1>

      </div>

      <div class="button">

        <button @click="next" > Next >> </button>

      </div>

    <button @click="show"> Teste </button>

  </div>
</template>

<script setup>

import {reactive, ref} from "vue";

const dados = reactive({
  q1: '',
  q2: '',
  q3: '',
  q4: '',
  q5: '',
  q6: '',
  q7: '',
  q8: '',
})


function show(){

  console.log(dados)

}

const isActive = ref(1);

function next() {

  const array = document.querySelector('.slide').childNodes;
  const index = ref(isActive.value);

  const button = document.querySelector('.button').childNodes;

  if (isActive.value === Number(array[index.value - 1].id)) {

    array[index.value - 1].hidden = 'true';

    if(isActive.value === 5 && dados.q5 === 'sim'){
      index.value++;
      isActive.value++;
    }

    isActive.value++;

    array[index.value].hidden = '';
  }

  if (isActive.value > (array.length - 1) ){
    button[0].hidden = 'true';
  }
}

</script>