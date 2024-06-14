<template>
  <div class="grid h-screen bg-black py-24 px-32 bg-cover bg-gradient-to-r from-black via-sky-950 to-sky-600">
    <form class="slide">



  

      <div id="1">
        <h1 class="text-white text-2xl tracking-wide mb-10"> Qual seu nome?</h1>

        <div class="relative z-0 w-full mb-5 group" id="1">
          
          <input autofocus type="email" class="block py-2.5 px-0 w-max text-sm bg-transparent border-0 border-b-2 border-sky-300 appearance-none dark:text-white dark:border-sky-600 dark:focus:border-sky-500 focus:outline-none focus:ring-0 focus:border-sky-600 peer text-white" placeholder="" required  v-model="dados.q1" />

          <label class="peer-focus:font-medium absolute text-xl text-sky-500 dark:text-sky-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-sky-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-8 ">Seu nome</label>

        </div>

      </div>

      <div id="2" hidden>
        <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu whats?</h1>
        <div class="relative z-0 w-full mb-5 group">

          <input class="block py-2.5 px-0 w-max text-sm bg-transparent border-0 border-b-2 border-sky-300 appearance-none dark:text-white dark:border-sky-600 dark:focus:border-sky-500 focus:outline-none focus:ring-0 focus:border-sky-600 peer text-white" placeholder="" required v-model="dados.q2">

          <label class="peer-focus:font-medium absolute text-xl text-sky-500 dark:text-sky-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-sky-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-8">Seu whats</label>

        </div>

      </div>

      <div id="3" hidden>

        <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu site?</h1>
        <div class="relative z-0 w-full mb-5 group">

          <input class="block py-2.5 px-0 w-max text-sm bg-transparent border-0 border-b-2 border-sky-300 appearance-none dark:text-white dark:border-sky-600 dark:focus:border-sky-500 focus:outline-none focus:ring-0 focus:border-sky-600 peer text-white" placeholder="" required v-model="dados.q3">

          <label class="peer-focus:font-medium absolute text-xl text-sky-500 dark:text-sky-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-sky-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-8">Seu site</label>
        </div>

      </div>

      <div id="4" hidden>

        <h1 class="text-white text-xl tracking-wide mb-10"> Qual seu instagram?</h1>
        <div class="relative z-0 w-full mb-5 group">

          <input class="block py-2.5 px-0 w-max text-sm bg-transparent border-0 border-b-2 border-sky-300 appearance-none dark:text-white dark:border-sky-600 dark:focus:border-sky-500 focus:outline-none focus:ring-0 focus:border-sky-600 peer text-white" placeholder="" required v-model="dados.q4">

          <label class="peer-focus:font-medium absolute text-xl text-sky-500 dark:text-sky-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-sky-600 peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-8">Seu insta</label>
        </div>

      </div>

      <div id="5" hidden>

        <h1 class="text-white text-xl tracking-wide mb-10"> Seu negócio fatura mais de R$ 15.000 por mês? </h1>
        <div class="flex flex-col gap-4">

          <li>
            <input class="peer hidden" type="radio" name="input1" id="input1" value="sim" v-model="dados.q5" />
            <label for="input1" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Sim </label>
          </li>

          <li>
    
            <input class="peer hidden" type="radio" name="input2" id="input2"  value="nao" v-model="dados.q5" />
            <label for="input2" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200  peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Não </label>
            
          </li>
            
        </div>

      </div>

      <div id="6" hidden>

        <h1 class="text-white text-xl tracking-wide mb-10"> Qual a média de faturamento mensal do seu negócio ? </h1>
        <div class="flex flex-col gap-4">

          <li>
            <input class="peer hidden" type="radio" name="input5" id="input5" value="A" v-model="dados.q6" />
            <label for="input5" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre R$ 15.000 a R$ 30.000 </label>
          </li>

          <li>

            <input class="peer hidden" type="radio" name="input6" id="input6"  value="B" v-model="dados.q6" />
            <label for="input6" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre R$ 30.000 a R$ 50.000 </label>
          </li>
            

          <li>
            <input class="hidden peer" type="radio" name="input7" id="input7" value="C" v-model="dados.q6" />
            <label for="input7" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre R$ 50.000 a R$ 100.000 </label>
          </li>

          <li>
            <input class="hidden peer" type="radio" name="input8" id="input8" value="D" v-model="dados.q6" />
            <label for="input8" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Acima de R$ 100.000 </label>
          </li>


        </div>

      </div>

      <div id="7" hidden>

        <h1 class="text-white text-xl tracking-wide mb-10"> Quanto investe mensalmente em tráfego pago?  </h1>

        <div class="flex flex-col gap-4">

          <li>

            
            <input class="peer hidden" type="radio" name="input9" id="input9"  value="A" v-model="dados.q7" />
            <label for="input9" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Não invisto ainda. </label>
          </li>



          <li>

            
            <input class="peer hidden" type="radio" name="input10" id="input10"  value="B" v-model="dados.q7" />
            <label for="input10" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre R$ 500 A R$1.000  </label>
          </li>


          <li>

            
            <input class="peer hidden" type="radio" name="input11" id="input11"  value="C" v-model="dados.q7" />
            <label for="input11" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre R$ 2.000 a R$ 5.000 </label>
          </li>


          <li>

            
            <input class="peer hidden" type="radio" name="input12" id="input12"  value="D" v-model="dados.q7" />
            <label for="input12" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre R$ 5.000 a R$ 10.000  </label>
          </li>


          <li>

            
            <input class="peer hidden" type="radio" name="input13" id="input13"  value="E" v-model="dados.q7" />
            <label for="input13" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Acima de R$ 10.000 </label>
          </li>

        </div>
      </div>


      <div id="8" hidden>


        <h1 class="text-white text-xl tracking-wide mb-10"> Há quanto tempo sua marca está no mercado?  </h1>

        <div class="flex flex-col gap-4">

          <li>

            <input class="peer hidden" type="radio" name="input14" id="input14"  value="A" v-model="dados.q8" />
            <label for="input14" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Menos de 1 ano </label>
          </li>

          <li>

            <input class="peer hidden" type="radio" name="input15" id="input15"  value="B" v-model="dados.q8" />
            <label for="input15" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre 1 a 2 anos  </label>
          </li>

          <li>

            <input class="peer hidden" type="radio" name="input16" id="input16" value="C" v-model="dados.q8" />
            <label for="input16" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Entre 2 a 3 anos </label>
          </li>

          <li>

            <input class="peer hidden" type="radio" name="input17" id="input17"  value="D" v-model="dados.q8" />
            <label for="input17" class="text-xl inline-flex items-center justify-between p-4 text-white bg-white border border-sky-200 rounded-lg cursor-pointer dark:hover:text-sky-300 dark:border-sky-700 dark:peer-checked:text-white peer-checked:border-sky-200 peer-checked:border-collapse box-border peer-checked:text-white hover:text-white hover:bg-sky-200 dark:text-e-400 dark:bg-transparent dark:hover:bg-sky-700 w-max min-w-full transition ease-in-out delay-75"> Mais de 3 anos   </label>
          </li>


        </div>


      </div>

      <div class="text-center pt-14" id="7" hidden>

        <h2 class="font-medium text-2xl text-white">  Tem pressa? fale agora com nosso consultor no WhatsApp!!! </h2>

        <p class="py-8 text-white"> Clique no botão abaixo! </p>

        <button class=" gap-2 items-center text-sky-700 hover:text-white border border-sky-700 hover:bg-sky-800 focus:outline-none focus:ring-sky-300 font-medium rounded-lg py-2.5 text-center me-2 mb-2 dark:border-sky-700 dark:text-white dark:hover:text-white dark:hover:bg-sky-600 dark:focus:ring-sky-800 text-xl px-8 transition ease-in-out delay-100"> Chamar consultor</button>

      </div>


    </form>

    <div class="button">

      <button class="flex gap-2 items-center text-sky-700 hover:text-white border border-sky-700 hover:bg-sky-800 focus:outline-none focus:ring-sky-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2 dark:border-sky-700 dark:text-white dark:hover:text-white dark:hover:bg-sky-600 dark:focus:ring-sky-800" @click="next" > Next

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




const isActive = ref(1);

function next() {

  console.log(dados)

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