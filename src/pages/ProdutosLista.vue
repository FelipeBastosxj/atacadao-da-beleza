<template>
  <q-page padding>
    <section class="text-h6">Lista de Produtos Disponiveis</section>

    <section class="row">
      <q-card v-for="images,index in imageNames" :key="index" class="my-card" flat bordered>
        <img style="height: 500px;" class="object-fit" :src="images" />

        <q-separator />
        <q-list>
          <q-item clickable>
            <q-item-section avatar>
              <q-icon color="positive" name="check_circle" />
            </q-item-section>

            <q-item-section>
              <q-item-label>Solicitar</q-item-label>
              <q-item-label caption>Disponivel.</q-item-label>
            </q-item-section>
          </q-item>

         
        </q-list>
      </q-card>
    </section>

    <div style="width: 100%;" class="row justify-center q-mt-md">
    <q-btn @click="goProduct" size="lg" class="row justify-center" color="accent" label="Inicio" icon="home"/>


  </div>
  </q-page>
</template>

<script>
import { useRouter } from 'vue-router';

export default {
  setup() {
    const router = useRouter()

    const goProduct = async()=>{
  router.push({name:"home"})
}

    return {
      goProduct,

      imageNames: [
        "images/1.png",
        "images/2.png",
        "images/3.png",
        "images/4.png",
        "images/5.png",
        "images/6.png",
        "images/7.png",
        "images/8.png",
        "images/9.png",
        "images/10.png",
        "images/11.png",
        "images/12.png",
        "images/13.png",
        "images/16.png",
      ],
    };
  },
};
</script>

<style scoped>
.my-card {
  width: 100%;
  max-width: 300px;
  margin: 30px;
}


</style>
