<template>
  <q-page padding>
    <section class="text-h6">Lista de Produtos Disponiveis</section>

    <section class="row">
      <q-card v-for="images,index in imageNames" :key="index" class="my-card" flat bordered>
        <img style="height: 500px;" class="object-fit" :src="'../../public/images/'+images" />

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
  </q-page>
</template>

<script>
export default {
  setup() {
    return {
      imageNames: [
        "1.png",
        "2.png",
        "3.png",
        "4.png",
        "5.png",
        "6.png",
        "7.png",
        "8.png",
        "9.png",
        "10.png",
        "11.png",
        "12.png",
        "13.png",
        "16.png",
        "17.png",

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
