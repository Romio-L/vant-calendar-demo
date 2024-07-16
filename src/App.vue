<script setup>
import { ref } from "vue";

const minDate = ref(new Date());

</script>

<template>

  <van-calendar 
    title="日历月份Bug演示" 
    :poppable="false" 
    :show-confirm="false" 
    :min-date="minDate"
    switch-mode="month"
  />

  <div class="tips">
    设置 switch-mode="month"和min-date时，当月份往更大月份切换之后，无法切回min-date设置时间的月份
  </div>

</template>

<style scoped>
.van-calendar {
  border: 1px #ddd solid;
  border-radius: 10px;
}

.tips{
  color: red;
  margin-top:20px;
  text-align: left;
}
</style>
