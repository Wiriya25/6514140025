<template>
  <div class="mockup-phone">
    <div class="camera"></div>
    <div class="display">
      <div class="artboard artboard-demo phone-1">
        <div v-for="m, index in display">
          <div class="chat chat start" v-if="index % 2 == 0">
            <div class="chat-bubble chat-bubble-info">{{ m }}</div>
          </div>
          <div class="chat chat-end" v-if="index % 2 == 1">
            <div class="chat-bubble chat-bubble-accent">{{ m }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
const message = [
  "สวัสดีค่ะ คุณชื่ออะไรหรอคะ ",
  "ผมชื่อวิริยะ นาคนพมณี",
  "คุณอายุเท่าไหร่",
  "ผมอายุ21ปีครับ",
]
const display = ref([]);
onMounted(() => {
  let count = 0;
  setInterval(() => {
    if (count + 1 > message.length) {
      count = 0;
      display.value = [];
    }
    display.value.push(message[count]);
    count++;
  }, 2000)
})
</script>
<style scoped>
.artboard-demo {
  justify-content: flex-end !important;
  align-items: unset !important;
  padding: 30px 20px;
}
</style>