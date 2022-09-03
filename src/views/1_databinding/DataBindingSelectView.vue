<template>
    <div>
        <select name="" id="" v-model="selectedCity">
            <option value=""></option>
            <option value="02">서울</option>
            <option value="051">부산</option>
            <option value="064">제주</option>
        </select>
        <br>
            <button @click="writeMe">클릭</button>
    </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: '02'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  methods: {
    writeMe() {
      console.log(this.selectedCity)
    }
  }
}
</script>
