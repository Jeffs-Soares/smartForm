<template>
  <div class="grid h-screen bg-teal-400 py-24 px-32 ">
      <div class="slide">


        <div id="1">
          <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu nome?</h1>
           <!--  <input autofocus class="bg-teal-400 placeholder:text-white focus:outline-none caret-white text-white focus:font-bold" placeholder="Seu nome aqui..." v-model="dados.q1"> -->
        
            <div class="relative z-0 w-full mb-5 group" id="1">
              <input autofocus type="email" class="block py-2.5 px-0 w-full text-sm bg-transparent border-0 border-b-2 border-teal-300 appearance-none dark:text-white dark:border-teal-600 dark:focus:border-teal-500 focus:outline-none focus:ring-0 focus:border-teal-600 peer placeholder:text-white focus:placeholder:text-teal-400 text-white" placeholder="Seu nome aqui..." required  v-model="dados.q1" />
             
              <label class="peer-focus:font-medium absolute text-sm text-teal-500 dark:text-teal-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-teal-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Seu nome</label>
          </div>

          </div>

        <div id="2" hidden>
          <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu whats?</h1>
          <div class="relative z-0 w-full mb-5 group">

            <input class="block py-2.5 px-0 w-full text-sm bg-transparent border-0 border-b-2 border-teal-300 appearance-none dark:text-white dark:border-teal-600 dark:focus:border-teal-500 focus:outline-none focus:ring-0 focus:border-teal-600 peer placeholder:text-white focus:placeholder:text-teal-400 text-white"  placeholder="Seu whats aqui..." required v-model="dados.q2">

            <label class="peer-focus:font-medium absolute text-sm text-teal-500 dark:text-teal-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-teal-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Seu whats</label>
          </div>

        </div>

        <div id="3" hidden>


          <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu site?</h1>
          <span class="block text-[12px] opacity-45 mb-2"> Se não possuir, deixe em branco...</span>
          <div class="relative z-0 w-full mb-5 group">

            <input class="block py-2.5 px-0 w-full text-sm bg-transparent border-0 border-b-2 border-teal-300 appearance-none dark:text-white dark:border-teal-600 dark:focus:border-teal-500 focus:outline-none focus:ring-0 focus:border-teal-600 peer placeholder:text-white focus:placeholder:text-teal-400 text-white"  placeholder="Seu site aqui..." required v-model="dados.q3">

            <label class="peer-focus:font-medium absolute text-sm text-teal-500 dark:text-teal-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-teal-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Seu site</label>
          </div>

        </div>

        <div id="4" hidden>

          <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu instagram?</h1>
          <div class="relative z-0 w-full mb-5 group">

            <input class="block py-2.5 px-0 w-full text-sm bg-transparent border-0 border-b-2 border-teal-300 appearance-none dark:text-white dark:border-teal-600 dark:focus:border-teal-500 focus:outline-none focus:ring-0 focus:border-teal-600 peer placeholder:text-white focus:placeholder:text-teal-400 text-white"  placeholder="Seu insta aqui..." required v-model="dados.q4">

            <label class="peer-focus:font-medium absolute text-sm text-teal-500 dark:text-teal-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-teal-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Seu insta</label>
          </div>

        </div>

        <div id="5" hidden>


<!--          <div class="space-y-4">-->
<!--            <label class="flex items-center space-x-2">-->
<!--              <input type="radio" name="option" class="hidden peer" />-->
<!--              <span class="text-gray-700 peer-checked:text-blue-500">Option 1</span>-->
<!--            </label>-->
<!--            <label class="flex items-center space-x-2">-->
<!--              <input type="radio" name="option" class="hidden peer" />-->
<!--              <span class="text-gray-700 peer-checked:text-blue-500">Option 2</span>-->
<!--            </label>-->
<!--            <label class="flex items-center space-x-2">-->
<!--              <input type="radio" name="option" class="hidden peer" />-->
<!--              <span class="text-gray-700 peer-checked:text-blue-500">Option 3</span>-->
<!--            </label>-->
<!--          </div>-->


          <h1 class="text-white text-xl tracking-wide mb-10"> Seu negócio fatura mais de R$ 15.000 por mês? </h1>
          <div class="flex flex-col gap-4">

          <input class="hidden peer" type="radio"  value="sim" v-model="dados.q5" />
          <label class="text-sm inline-flex items-center justify-between p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full peer-checked:bg-red-600" for="one"> Sim </label>

          <input class="hidden peer" type="radio"  value="nao" v-model="dados.q5" />
          <label class="text-sm inline-flex items-center justify-between p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full " for="two"> Não </label>

          </div>

        </div>

        <div id="6" hidden>

          <h1 class="text-white text-xl tracking-wide mb-10"> Qual a média de faturamento mensal do seu negócio ? </h1>
          <div class="flex flex-col gap-4">

              <input class="hidden peer" type="radio"  value="A" v-model="dados.q6" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="A"> Entre R$ 15.000 a R$ 30.000 </label>

              <input class="hidden peer" type="radio"  value="B" v-model="dados.q6" />
              <label class=" text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="B"> Entre R$ 30.000 a R$ 50.000 </label>

              <input class="hidden peer" type="radio"  value="C" v-model="dados.q6" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="C"> Entre R$ 50.000 a R$ 100.000 </label>

              <input class="hidden peer" type="radio"  value="D" v-model="dados.q6" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="D"> Acima de R$ 100.000 </label>


            </div>

        </div>

        <div id="7" hidden>

          <h1 class="text-white text-xl tracking-wide mb-10"> Quanto investe mensalmente em tráfego pago?  </h1>

          <div class="flex flex-col gap-4">


              <input class="hidden peer" type="radio"  value="A" v-model="dados.q7" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="A"> Não invisto ainda. </label>



              <input class="hidden peer" type="radio"  value="B" v-model="dados.q7" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="B"> Entre R$ 500 A R$1.000  </label>



              <input class="hidden peer" type="radio"  value="C" v-model="dados.q7" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="C"> Entre R$ 2.000 a R$ 5.000 </label>



              <input class="hidden peer" type="radio"  value="D" v-model="dados.q7" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="D"> Entre R$ 5.000 a R$ 10.000  </label>



              <input class="hidden peer" type="radio"  value="E" v-model="dados.q7" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 min-w-full " for="E"> Acima de R$ 10.000 </label>

            <input class="hidden peer" type="radio"  value="E" v-model="dados.q7" />
            <label class=" " for="E">  </label>



          </div>
        </div>


        <div id="8" hidden>

          
          <h1 class="text-white text-xl tracking-wide mb-10"> Há quanto tempo sua marca está no mercado?  </h1>

          <div class="flex flex-col gap-4">


              <input class="hidden peer" type="radio"  value="A" v-model="dados.q8" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="A"> Menos de 1 ano </label>



              <input class="hidden peer" type="radio"  value="B" v-model="dados.q8" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="B"> Entre 1 a 2 anos  </label>



              <input class="hidden peer" type="radio"  value="C" v-model="dados.q8" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="C"> Entre 2 a 3 anos </label>



              <input class="hidden peer" type="radio"  value="D" v-model="dados.q8" />
              <label class="text-sm inline-flex items-center justify-between w-full p-5 text-teal-500 bg-white border border-teal-200 rounded-lg cursor-pointer dark:hover:text-teal-300 dark:border-teal-700 dark:peer-checked:text-teal-500 peer-checked:border-teal-600 peer-checked:text-teal-600 hover:text-teal-600 hover:bg-teal-100 dark:text-teal-400 dark:bg-teal-800 dark:hover:bg-teal-700 w-max min-w-full" for="D"> Mais de 3 anos   </label>


          </div>


        </div>

        <div class="text-center" id="7" hidden>

          <h2 class="font-medium text-2xl">  Tem pressa? fale agora com nosso consultor no WhatsApp!!! </h2>

          <p class="py-8"> Clique no botão abaixo! </p>

          <button class=" gap-2 items-center text-teal-700 hover:text-white border border-teal-700 hover:bg-teal-800 focus:outline-none focus:ring-teal-300 font-medium rounded-lg px-5 py-2.5 text-center me-2 mb-2 dark:border-teal-700 dark:text-teal-700 dark:hover:text-white dark:hover:bg-teal-600 dark:focus:ring-teal-800 text-xl"> Chamar consultor</button>

        </div>


      </div>

      <div class="button">

        <button class="flex gap-2 items-center text-teal-700 hover:text-white border border-teal-700 hover:bg-teal-800 focus:outline-none focus:ring-teal-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2 dark:border-teal-700 dark:text-teal-700 dark:hover:text-white dark:hover:bg-teal-600 dark:focus:ring-teal-800" @click="next" > Next

          <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
            </svg>

        </button>

      </div>


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

    console.log(button[0])
    button[0].className = 'hidden';
  }
}

</script>
