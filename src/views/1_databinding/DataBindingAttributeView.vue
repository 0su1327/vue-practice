<template>
  <div>
      <input type="text" name="" id="" v-bind:value="userId" readonly />
      <input type="text" name="" id="" :value="userId" readonly />
      <br>
      <img :src="imgSrc" alt="" style="width:100px; height:auto;" />
      <br>
      <input type="search" name="" id="" v-model="txt1">
      <button :disabled="txt1 === ''">조회</button> <!--txt1이 비어있는가?? -> txt1이 비어있으면 true임으로 disabled가 실행되고 아니면 enable 실행.-->
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'abcdefeafdsf',
      imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/f/f1/Vue.png',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  methods: {}
}
</script>
