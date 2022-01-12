<template>
  <div>
    <div class="hero-image">
      <div class="hero-text">
        <h1>Ayo Kita Travel</h1>
        <p>Temukan Destinasi Impianmu</p>
        <button><a href="#destinasi">Pesan Sekarang</a></button>
      </div>
    </div>
  </div>
</template>

<script>
import CustomButton from "../components/Button.vue";
import axios from "axios";
export default {
  data() {
    return {
      label: "About",
      dataUSA: []
    };
  },
  components: {
    CustomButton
  },
  async created() {
    try {
      const urlAPI =
        "https://datausa.io/api/data?drilldowns=Nation&measures=Population";
      const response = await axios.get(urlAPI);
      const {
        data: { data: arrData }
      } = response;
      this.dataUSA = arrData;
    } catch (err) {
      console.log(err);
    }
  }
};
</script>

<style></style>
