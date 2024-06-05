<template>
  <div class="grid h-screen bg-teal-400 py-24 px-32 ">
      <div class="slide">

        <div id="1">
          <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu nome?</h1>
           <!--  <input autofocus class="bg-teal-400 placeholder:text-white focus:outline-none caret-white text-white focus:font-bold" placeholder="Seu nome aqui..." v-model="dados.q1"> -->
        
            <div class="relative z-0 w-full mb-5 group" id="1">
              <input autofocus type="email" class="block py-2.5 px-0 w-full text-sm bg-transparent border-0 border-b-2 border-teal-300 appearance-none dark:text-white dark:border-teal-600 dark:focus:border-teal-500 focus:outline-none focus:ring-0 focus:border-teal-600 peer placeholder:text-white focus:placeholder:text-teal-400 text-white" placeholder="Seu nome aqui..." required  v-model="dados.q1" />
             
              <label for="floating_email" class="peer-focus:font-medium absolute text-sm text-teal-500 dark:text-teal-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-teal-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Seu nome</label>
          </div>

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

        <button class="flex gap-2 items-center text-teal-700 hover:text-white border border-teal-700 hover:bg-teal-800 focus:ring-4 focus:outline-none focus:ring-teal-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2 dark:border-teal-700 dark:text-teal-700 dark:hover:text-white dark:hover:bg-teal-600 dark:focus:ring-teal-800" @click="next" > Next

          <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
            </svg>

        </button>

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
