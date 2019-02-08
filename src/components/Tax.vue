<template>
  <div class="hello">
    <p>base price: <input type="text" v-model="basePrice" /></p>
    <p>include price: <input type="text" v-model="includePrice" /></p>
  </div>
</template>

<script>
export default {
  name: "Tax",
  data() {
    return {
      basePrice: 100
    };
  },
  computed: {
    includePrice: {
      get: function() {
        return parseInt(this.basePrice * 1.08);
      },
      set: function(includePrice) {
        return (this.basePrice = Math.ceil(includePrice / 1.08));
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
