<template>
  <div>
    <v-btn v-for="(consonant,index) in consonants" key="index" small outlined color="blue" @click="clicked(index)">
      {{ consonant }}
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "ConsonantSelector",
  data() {
    return {
      consonants: "ㄱㄴㄷㄹㅁㅂㅅㅇㅈㅊㅋㅌㅍㅎ".split('')
    }
  },
  methods: {
    clicked(event,index){
      console.log(index);
    }
  }

}
</script>

<style scoped>

</style>
