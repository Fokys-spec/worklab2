<template>
  <div id="app">
    <h1>Календар</h1>
    <div class="date-display">
      {{ formattedDate }}
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      currentDate: new Date(), // Зберігає поточну дату
    };
  },
  computed: {
    formattedDate() {
    
      const options = { year: "numeric", month: "long", day: "numeric" };
      return this.currentDate.toLocaleDateString("uk-UA", options);
    },
  },
};
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 20px;
  background-color: #f0f0f5;
}

#app {
  margin-top: 50px;
}

.date-display {
  font-size: 2em;
  color: #333;
  margin-top: 20px;
}
</style>
