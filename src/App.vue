<template>
  <BodyMassIndex msg="Cálculo do IMC" />
</template>

<script>
import BodyMassIndex from "./components/BodyMassIndex.vue";

export default {
  name: "App",
  components: {
    BodyMassIndex,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 40px 0 0 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
