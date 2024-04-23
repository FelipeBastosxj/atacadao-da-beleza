<template>
  <q-layout class="bg-grey-1">
    <q-header elevated class="text-white" style="background: #D97F76" height-hint="61.59">
      <q-toolbar class="q-py-sm q-px-md">
        <q-btn round dense flat :ripple="false"  size="19px" color="white" class="q-mr-sm" no-caps >
          <q-avatar size="52px">
        <img src="../../public/icons/favicon-96x96.png">
      </q-avatar>
        </q-btn>

    

        <span class="text-h6">Atacadão da Beleza</span>

        <q-space />

        
        <div v-if="$q.screen.gt.sm" class="GL__toolbar-link q-ml-xs q-gutter-md text-body2 text-weight-bold row items-center no-wrap">
          <a @click="routerGo('home')" style="cursor: pointer;" href="javascript:void(0)" class="text-white">
            Home
          </a>
        
          <a style="cursor: pointer;" @click="routerGo('produtos')" class="text-white">
            Produtos
          </a>
         
        </div>

        <div class="q-pl-sm q-gutter-sm row items-center no-wrap">
          <q-btn v-if="$q.screen.gt.xs" dense flat round size="sm" icon="notifications" />
          

         
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from 'vue'
import { useRouter } from 'vue-router';



export default {
  name: 'MyLayout',

  setup () {
    const text = ref('')
    const router = useRouter()

    const search = ref(null) // $refs.search

   const routerGo = async(value)=>{
    router.push({name:value})
   }

    return {
      routerGo,

      text,
    

      search,

  
    }
  }
}
</script>

