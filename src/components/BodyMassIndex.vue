<template>
  <div>
    <h1 class="message">{{ msg }}</h1>
    <h3>Digite sua altura e peso</h3>
    <div class="p-fluid">
      <InputText
        :style="{ marginBottom: '.5em' }"
        id="height"
        type="text"
        v-model="height"
        placeholder="Altura"
      />
      <InputText id="weight" type="text" v-model="weight" placeholder="Peso" />

      <Button
        :style="{ marginTop: '1em' }"
        label="Calcular IMC"
        @click="IMCCalculate"
      />
    </div>

    <p>
      Seu IMC é: <span :style="{ fontWeight: '800' }">{{ imc }}</span>
    </p>
  </div>
</template>

<script>
export default {
  name: "BodyMassIndex",
  props: {
    msg: String,
  },
  data() {
    return {
      height: null,
      weight: null,
      imc: null,
    };
  },

  methods: {
    IMCCalculate() {
      this.imc = (this.weight / (this.height * this.height)).toFixed(2);
    },
  },
};
</script>

<style scoped>
.message {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 40px 0 0 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}

h3 {
  margin-bottom: 24px;
  font-weight: 400;
}
</style>
