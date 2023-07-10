<template>
  <MainLayout>
    <div id="IndexPage" class="mt-4 max-w-[1200px] mx-auto px-2">
      <div class="grid xl:grid-cols-6 lg:grid-cols-5 md:grid-cols-4 sm:grid-cols-3 grid-cols-2 gap-4">
                <div v-if="products" v-for="product in products" :key="product">
                    <ProductComponent :product="product"/>
                </div>
            </div>  
    </div>
  </MainLayout>
</template>

<script setup>
import MainLayout from "~/layouts/MainLayout.vue";
import { useUserStore } from '~/stores/user';
const userStore = useUserStore()

let products = [
  {id:1 , title: 'Title 1' , description: 'Bla bla' , url : 'https://picsum.photos/id/7/800/800' , price: 898},
  {id:2 , title: 'Title 1' , description: 'Bla bla1' , url : 'https://picsum.photos/id/8/800/800' , price: 111},
  {id:4 , title: 'Title 1' , description: 'Bla bla3' , url : 'https://picsum.photos/id/9/800/800' , price: 111},
  {id:6 , title: 'Title 1' , description: 'Bla bla4' , url : 'https://picsum.photos/id/3/800/800' , price: 123123},
  {id:7 , title: 'Title 1' , description: 'Bla bla5' , url : 'https://picsum.photos/id/4/800/800' , price: 81238},
  {id:90 , title: 'Title 1' , description: 'Bla bla6' , url : 'https://picsum.photos/id/2/800/800' , price: 1238},
]
// onBeforeMount(async () => {
//     products.value = await useFetch('/api/prisma/get-all-products')
//     setTimeout(() => userStore.isLoading = false, 1000)
// })
</script>

<style lang="scss" scoped></style>
