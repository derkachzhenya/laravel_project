<template>
  <div>
    <h1 class="text-3xl font-bold underline">Текущее время: {{ currentTime }}</h1>
    <h2 class="text-2xl">Прошло секунд: {{ elapsedSeconds }}</h2>
    апа
  </div>
</template>

<script>
export default {
  name: "RealTimeUpdate",
  data() {
    return {
      currentTime: new Date().toLocaleTimeString(),
      elapsedSeconds: 0,
    };
  },
  mounted() {
    // Обновляем время каждую секунду
    setInterval(() => {
      this.currentTime = new Date().toLocaleTimeString();
      this.elapsedSeconds++;
    }, 1000);
  },
};
</script>