<template>
  <div class="container">
    <h1>Summer Sale</h1>
    <img src="https://image.uniqlo.com/UQ/ST3/eu/imagesgoods/445173/item/eugoods_63_445173.jpg?width=1083&impolicy=quality_60&imformat=chrome" width="200px">
    <div>
      <strike v-show="oldDiscount">Was {{ oldDiscount }}%</strike>
      <strong> Now {{ discount }}% OFF</strong><br/>
      <a href="#" @click="updateDiscount">Discount Counter</a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      oldDiscount: 0,
      discount: 5,
    }
  },
  watch: {
    discount: {
      handler: function (newVal, oldVal){
        console.log(`actual(${newVal}%) and old(${oldVal}%) discount.`);
        this.oldDiscount = oldVal;
      },
      immediate: false,
      deep: true
    }
  },
  methods: {
    updateDiscount(){
      this.discount = this.discount + 15;
    }
  }
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
  background: #c04f97;
  border-radius: 10px;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
}
</style>

