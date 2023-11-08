<template>
  <main>
    <div class="rill">
      <div>
        <h1>We Can Count!!</h1>
      </div>
      <div>
        <h3>Lets put some numbers</h3>
      </div>
      <div>
        <input v-model="num1" type="number" class=" fs-5 ">
        <input v-model="num2" type="number" class=" fs-5 "> 
      </div>
      <br><br>
      <button @click="addNum()" class=" btn btn-primary m-1 "> + </button>
      <button @click="minNum()" class=" btn btn-primary m-1 "> - </button>
      <button @click="kaliNum()" class=" btn btn-primary m-1 "> * </button>
      <button @click="bagiNum()" class=" btn btn-primary m-1 "> / </button>
      <br><br>
      <h1>{{ num1 }} {{ task }} {{ num2 }} = {{ result }}</h1>
      <button @click="setcol1()" class=" btn btn-primary m-1 ">Set Column 1 as Result</button>
      <button @click="setcol2()" class=" btn btn-primary m-1 ">Set Column 2 as Result</button>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      result: 0,
      task: "?",
    }
  },
  methods: {
    addNum() {
      if(isNaN(this.num1)) parseInt(this.num1);
      if(isNaN(this.num2)) parseInt(this.num2);
      this.task = "+"
      this.result = this.num1 + this.num2
    },
    minNum() {
      if(isNaN(this.num1)) parseInt(this.num1);
      if(isNaN(this.num2)) parseInt(this.num2);
      this.task = "-"
      this.result = this.num1 - this.num2
    },
    kaliNum() {
      if(isNaN(this.num1)) parseInt(this.num1);
      if(isNaN(this.num2)) parseInt(this.num2);
      this.task = "x"
      this.result = this.num1 * this.num2
    },
    bagiNum() {
      if(isNaN(this.num1)) parseInt(this.num1);
      if(isNaN(this.num2)) parseInt(this.num2);
      this.task = "÷"
      this.result = this.num1 / this.num2
    },
    setcol1() {
      this.num1 = this.result
    },
    setcol2() {
      this.num2 = this.result
    }
  }
}
</script>