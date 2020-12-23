<template>
  <div class="informer-container">
    <Temperature v-bind:real="weather.temp_real" v-bind:feel="weather.temp_feel"/>
    <FlexBreak />
    <Humidity v-bind:val ="humidity" />
    <VertDiv />
    <Wind v-bind:val="wind"/>
  </div>
</template>

<script>
import Temperature from "./Temperature.vue";
import Humidity from "./Humidity.vue";
import Wind from "./Wind.vue";
import FlexBreak from "./FlexBreak.vue";
import VertDiv from "./VertDiv.vue";
export default {
  name: "Container",
  components: {
    Temperature,
    Humidity,
    Wind,
    FlexBreak,
    VertDiv,
  },
  props: ['weather'],
};
</script>

<style>
.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  padding: 30px;
  background-image: url("/img/forest.png");
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}
</style>