<template>
  <div class="main-container">
    <div class="border">
      <div>
        <h2>Simple Calculator App</h2>
        <div class="container-wrapper">
          <div class="top">
            <div class="result">{{ result }}</div>
          </div>
          <div class="container">
            <div class="left">
              <div class="calculatorbutton1">
                <div class="bottom">
                  <button @click="zero">0</button>
                </div>
                <div class="bottom">
                  <button @click="one">1</button>
                </div>
                <div class="bottom">
                  <button @click="two">2</button>
                </div>
              </div>
              <div class="calculatorbutton2">
                <div class="bottom">
                  <button @click="three">3</button>
                </div>
                <div class="bottom">
                  <button @click="four">4</button>
                </div>
                <div class="bottom">
                  <button @click="five">5</button>
                </div>
              </div>
              <div class="calculatorbutton3">
                <div class="bottom">
                  <button @click="six">6</button>
                </div>
                <div class="bottom">
                  <button @click="seven">7</button>
                </div>
                <div class="bottom">
                  <button @click="eight">8</button>
                </div>
              </div>
              <div class="calculatorbutton4">
                <div class="bottom">
                  <button @click="nine">9</button>
                </div>

                <div class="bottom">
                  <button @click="equal">=</button>
                </div>
                <div class="bottom">
                  <button @click="clear">C</button>
                </div>
              </div>
            </div>
            <div class="right">
              <div class="bottom"><button @click="plus">+</button></div>

              <div class="bottom">
                <button @click="minus">-</button>
              </div>

              <div class="bottom">
                <button @click="divide">/</button>
              </div>
              <div class="bottom">
                <button @click="multiplication">X</button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div style="font-size: 12px">Designed by N.S.O</div>
    </div>
  </div>
</template>


<script>
export default {
  name: "CalculatorApp",
  data: function () {
    return {
      text1: "",
      text2: "",
      result: "",
      array: [],
    };
  },
  methods: {
    calculate() {
      var one = parseInt(this.text1);
      var two = parseInt(this.text2);
      this.result = one + two;
    },

    zero() {
      if (!this.result) return
      this.result += 0;
    },

    one() {
      this.result += 1;
    },

    two() {
      this.result += 2;
    },

    three() {
      this.result += 3;
    },

    four() {
      this.result += 4;
    },

    five() {
      this.result += 5;
    },

    six() {
      this.result += 6;
    },

    seven() {
      this.result += 7;
    },

    eight() {
      this.result += 8;
    },

    nine() {
      this.result += 9;
    },

    plus() {
       if (!this.result) return
      this.result += " + ";
    },

    minus() {
       if (!this.result) return
      this.result += " - ";
    },

    divide() {
      if (!this.result) return
      this.result += " / ";
    },

    multiplication() {
       if (!this.result) return
      this.result += " * ";
    },

    clear() {
      this.result = "";
    },

    equal() {
      this.result = this.result && eval(this.result);
    },

  },
};
</script>
  
<style>
.main-container {
  height: 80vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-content: center;
}
.bottom {
  margin-bottom: 4px;
}
.border {
  background-color: aqua;
  width: 400px;
}
.calculatorbutton1 {
  display: flex;
}
.calculatorbutton2 {
  display: flex;
}

.calculatorbutton3 {
  display: flex;
}

.calculatorbutton4 {
  display: flex;
}
.container {
  display: flex;
  justify-content: center;
}
.right {
  display: flex;
  flex-direction: column;
}
button {
  width: 80px;
  height: 50px;
  margin-right: 2px;
}
.result {
  background-color: rgb(150, 150, 186);
  display: flex;
  justify-self: center;
  width: 80%;
  min-height: 40px;
  color: whitesmoke;
  font-weight: bolder;
  text-align: center;
  justify-content: flex-end;
  align-items: center;
  padding: 3px;
}
.container-wrapper {
  display: flex;
  flex-direction: column;
}
.top {
  display: flex;
  justify-content: center;
  margin-bottom: 2px;
}
</style>