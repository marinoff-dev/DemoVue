<template>
    <div>
      <vmodal v-if="showModal" title="Ajouter un membre" @close="close">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Id quos, minus at repellat voluptatem iusto? Esse autem illo, reiciendis explicabo suscipit optio quasi distinctio consectetur earum, similique deserunt temporibus perspiciatis.</vmodal>
      <h1 class="text-2xl uppercase font-semibold">Application 1</h1>
  
      <div class=" container mx-auto my-4 flex justify-between">
        <input type="text" class="border border-gray-700 p-3 outline-none" placeholder="recherche...">
        <button @click="showModal = true" class="bg-blue-500 p-3 text-white ">Ajouter un membre</button>
      </div>
  
     
      <UserTable :datas="Users" />
  
    </div>
  </template>
  
  <script setup>
  import {ref} from 'vue'
  import UserTable from './components/UserTable.vue'
  import Vmodal from '@/components/Vmodal.vue'
  const showModal = ref(false)
  const Users = ref(
    [
    {
      "id": 1,
      "name": "Leanne Graham",
      "username": "Bret",
      "email": "Sincere@april.biz",
      "phone": "1-770-736-8031 x56442",
      "website": "hildegard.org"
    },
    {
      "id": 2,
      "name": "Ervin Howell",
      "username": "Antonette",
      "email": "Shanna@melissa.tv",
  
      "phone": "010-692-6593 x09125",
      "website": "anastasia.net"
    }
  ]
  
  )
  
  function close() {
    showModal.value = false
  }
  
  
  </script>
  
  <style lang="scss" scoped>
  
  </style>