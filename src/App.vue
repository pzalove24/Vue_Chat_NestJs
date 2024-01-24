<script setup>
import { io } from "socket.io-client"
import { onBeforeMount, ref } from "vue";

const socket = io('http://localhost:3001')
const messages = ref([])

onBeforeMount(() => {
  socket.emit('findAllMessages')
})

</script>

<template>
  <div class="chat">

  </div>
</template>

<style ></style>
