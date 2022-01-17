<template>
  <div id="app">
    <div class="np-title">Realtime Date Time</div>
    <div class="np-time">
      {{ currentDateTime }}
    </div>
    <div class="np-credits">www.nightprogrammer.com</div>
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      currentDateTime: null,
    };
  },
  mounted() {
    setInterval(() => {
      this.currentDateTime = new Date();
    }, 1000);
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 12px;
}
.np-title {
  font-size: 20px;
}
.np-time {
  font-size: 24px;
  font-weight: 600;
  margin: 12px 0px;
  border: 1px solid #eee;
  background: #003cff;
  padding: 4px 10px;
  color: #fff;
  max-width: 490px;
  border-radius: 6px;
}
.np-credits {
  font-size: 12px;
}
</style>
