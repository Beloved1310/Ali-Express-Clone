<template>
    <MainLayout>
        <div id="IndexPage" class="mt-4 max-w-[1200px] mx-auto px-2">
            <div class="grid xl:grid-cols-6 lg:grid-cols-5 md:grid-cols-4 sm:grid-cols-3 grid-cols-2 gap-4">
                  <div v-if="products" v-for="product in products" :key="product">
                    <ProductComponent :product="product"/>
                </div>
                <!-- <div v-if="products" v-for="product in products.data" :key="product">
                    <ProductComponent :product="product"/>
                </div> -->
            </div>
        </div>
    </MainLayout>
</template>

<script setup>
import MainLayout from '~/layouts/MainLayout.vue';
import { useUserStore } from '~/stores/user';
const userStore = useUserStore()
const products = [
    {id: 1, title: "Title1", description: "This is a description 1", url:"https://picsum.photos/id/7/800/900", price: 9999 },
    {id: 2, title: "Title2", description: "This is a description 2", url:"https://picsum.photos/id/8/800/900", price: 9998 },
    {id: 3, title: "Title3", description: "This is a description 3", url:"https://picsum.photos/id/9/800/900", price: 9997 },
    {id: 4, title: "Title4", description: "This is a description 4", url:"https://picsum.photos/id/10/800/900", price: 9996 },
    {id: 5, title: "Title5", description: "This is a description 5", url:"https://picsum.photos/id/11/800/900", price: 9995 },
    {id: 6, title: "Title6", description: "This is a description 6", url:"https://picsum.photos/id/12/800/900", price: 9994 },
    {id: 7, title: "Title7", description: "This is a description 7", url:"https://picsum.photos/id/13/800/900", price: 9993 },
    {id: 8, title: "Title8", description: "This is a description 8", url:"https://picsum.photos/id/14/800/900", price: 9993 },
    {id: 9, title: "Title9", description: "This is a description 9", url:"https://picsum.photos/id/15/800/900", price: 9993 },
    {id: 10, title: "Title10", description: "This is a description 10", url:"https://picsum.photos/id/16/800/900", price: 9993 },
]
// let products = ref(null)
// onBeforeMount(async () => {
//     products.value = await useFetch('/api/prisma/get-all-products')
//     setTimeout(() => userStore.isLoading = false, 1000)
// })
</script>