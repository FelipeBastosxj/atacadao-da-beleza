<template>
  <q-page padding>
    <span style="font-size: 30px; color: #351C75;" class="titulo q-mb-lg row justify-center">Seja bem-vindo(a) à nossa empresa.</span>
    <span style="font-size: 16px; text-align: center; margin-bottom: 25px;" class="fade-in-down"
      >A empresa Atacadão da Beleza será uma distribuidora de cosméticos com
      alguns diferenciais do resto do mercado. Como objetivo, procuraremos
      sempre o melhor atendimento possível para os clientes, com consultoria
      especializada, auxiliando os mesmos a escolher o melhor produto mediante
      as suas necessidades. Focaremos também em agilidade e eficiência,
      trabalhando com os melhores prazos para melhor atender os clientes, além
      de confiança na entrega e garantir que entregaremos o melhor produto, sem
      nenhuma avaria. Temos metas para crescimento da empresa, garantindo
      futuramente um treinamento para os nossos vendedores e funcionários no
      geral, com professores e palestrantes de renome no mercado. Possuímos
      alguns princípios éticos, principalmente em relação ao meio ambiente e
      relações humanas. Buscamos sempre produtos de boa procedência, sem testes
      em animais e que possam ter o melhor efeito quando usados, comprovados
      pela Anvisa. Além disso, procuramos conhecer antes de tudo o cliente,
      tendo um atendimento personalizado e único para cada indivíduo.
    </span>

    <span style="font-size: 30px; color: #351C75;" class="titulo q-mb-lg">Socios:</span>

    <q-carousel
        v-model="slide"
        transition-prev="scale"
        transition-next="scale"
        swipeable
        animated
        control-color="white"
        navigation
        padding
        arrows
        height="600px"
        class="bg-primary text-white shadow-1 rounded-borders q-mt-lg"
      >
        <q-carousel-slide name="1" class="column no-wrap flex-center">
          <q-icon name="person" size="56px" />
          <div style="font-size: 30px;" class="q-mt-md text-center">
            Sandy (ceo)
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="2" class="column no-wrap flex-center">
          <q-icon name="person" size="56px" />
          <div style="font-size: 30px;" class="q-mt-md text-center">
            Nathan (gerente)
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="3" class="column no-wrap flex-center">
          <q-icon name="person" size="56px" />
          <div style="font-size: 30px;" class="q-mt-md text-center">
            Breno (supervisor)
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="4" class="column no-wrap flex-center">
          <q-icon name="person" size="56px" />
          <div style="font-size: 30px;" class="q-mt-md text-center">
            Felipe (Contador)
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="5" class="column no-wrap flex-center">
          <q-icon name="person" size="56px" />
          <div style="font-size: 30px;" class="q-mt-md text-center">
            Yasmin (Embalagem)
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="6" class="column no-wrap flex-center">
          <q-icon name="person" size="56px" />
          <div style="font-size: 30px;" class="q-mt-md text-center">
            Gustavo (vendedor)
          </div>
        </q-carousel-slide>
      </q-carousel>
  </q-page>
</template>

<script setup>
import {ref} from'vue'

defineOptions({
  name: "IndexPage",
});

const slide = ref('1')
const typeWriter = async(elemento)=>{
 const textoArray = elemento.innerHTML.split('')
 elemento.innerHTML = ''
textoArray.forEach((letra,i)=>{
  setTimeout(()=> elemento.innerHTML += letra, 75 * i)
 })
}

setTimeout(()=>{
  const titulo = document.querySelector('.titulo')

typeWriter(titulo)
},100)

</script>

<style>
.fade-in-down {
  display: inline-block;
  margin: 0 0.5rem;
  animation: fadeInLeft; /* referring directly to the animation's @keyframe declaration */
  animation-duration: 1s; /* don't forget to set a duration! */
}

.titulo{
  font-weight: bolder;
  text-align: center;
}
</style>
