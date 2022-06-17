<template>
  <div>
    11111
    <span class="fw-800">123456</span>
    <span class="fw-700">123456</span>

    <v-text-field class="fw-700"></v-text-field>
    <v-text-field class="fw-800"></v-text-field>
    <v-text-field ></v-text-field>
  </div>
</template>

<script>
export default {
  name: "font"
}
</script>

<style scoped>
@font-face {
  font-family: 'SUIT-Medium';
  src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_suit@1.0/SUIT-Medium.woff2') format('woff2');
  font-weight: normal;
  font-style: normal;
}

div{
  font-family: 'SUIT';
}

.fw-800{
  font-weight: 800;
}

.fw-700{
  font-weight: 600;
}
</style>
