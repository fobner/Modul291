<template>
  <div>
    <h1>T-Shirts</h1>
    <img src="https://image.uniqlo.com/UQ/ST3/eu/imagesgoods/445173/item/eugoods_63_445173.jpg?width=1083&impolicy=quality_60&imformat=chrome" width="200px">
    <ul>
      <li v-for="n in 3" :key="n">
        <a href="#" @click="triggerAlert(n)">Size {{ n }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    triggerAlert(n) {
      alert(`${n} has been clicked`)
    },
  },
}
</script>

<style lang="scss" scoped>
ul {
  padding-left: 0;
}
li {
  display: block;
  list-style: none;

  + li {
    margin-top: 10px;
  }
}

a {
  display: inline-block;
  background: #2f5859;
  border-radius: 10px;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
}
</style>
