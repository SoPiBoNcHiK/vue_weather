<template>
  <div class="wind"><img src="/img/wind.png" /> 12 <small>м/с</small></div>
</template>

<script>
export default {
  name: "Wind",
  data() {
    return {
      weather: {
        temp_real: 0,
        temp_feel: -3.5,
        humidity: 5,
        wind: 20,
      },
    };
  },
};
</script>

<style>
.wind {
  font-family: "Arial", sans-serif;
  font-size: 40px;
  font-weight: 400;
  color: #fff;
  position: relative;
  display: inline-block;
  line-height: 0.9;
  text-shadow: 2px 2px 2px #444;
  margin: 15px;
}

.wind img {
  width: 30px;
  margin-right: -5px;
  vertical-align: middle;
}
</style>