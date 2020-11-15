<template>
  <div class="w-full h-screen flex justify-center content-center bg-green-200">
    <div class="flex rounded-lg bg-gray-700 w-10/12 md:mx-0 md:w-6/12 mt-24 pt-5 border border-gray-400 justify-center flex-col items-center" style="max-height:600px">
      <!-- Display -->
      <div class="w-10/12 bg-gray-200 my-4 flex justify-end rounded-lg" style="min-height: 70px">
        <input type="text" class="uppercase font-bold w-full text-right" style="font-size: 45px" maxlength="8" :model="display" :value="display">
      </div>
      <!-- Keyboards -->
      <div class="w-10/12 h-full mb-4">
        <div class="row flex justify-end">
          <div class="button-controll bg-red-400" v-on:click="allClearDisplay">
            AC
          </div>
          <div class="button-controll bg-yellow-400" v-on:click="clearDisplay">
            C
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button" v-on:click="addValue" value="7">
            7
          </div>
          <div class="button" v-on:click="addValue" value="8">
            8
          </div>
          <div class="button" v-on:click="addValue" value="9">
            9
          </div>
          <div class="button" v-on:click="addValue" value="/">
            /
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button" v-on:click="addValue" value="4">
            4
          </div>
          <div class="button" v-on:click="addValue" value="5">
            5
          </div>
          <div class="button" v-on:click="addValue" value="6">
            6
          </div>
          <div class="button" v-on:click="addValue" value="*">
            X
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button" v-on:click="addValue" value="1">
            1
          </div>
          <div class="button" v-on:click="addValue" value="2">
            2
          </div>
          <div class="button" v-on:click="addValue" value="3">
            3
          </div>
          <div class="button" v-on:click="addValue" value="-">
            -
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button" v-on:click="addValue" value="0">
            0
          </div>
          <div class="button" v-on:click="addValue" value=".">
            .
          </div>
          <div class="button" v-on:click="addValue" value="+">
            +
          </div>
          <div class="button" v-on:click="addValue" value="=">
            =
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      display: 0
    }
  },
  mounted() {
    console.log('entrou', this.display)
  },
  methods: {
    addValue(e){
      if(this.display.toString().length < 12){
        const {value} = e.target.attributes.value;
        this.display =  `${this.display}${value}`
      }
    },
    allClearDisplay() {
      this.display = 0;
    }, 
    clearDisplay() {
      this.display = this.display.substring(0, this.display.length - 1)
    } 
  }
};
</script>

<style>
.button {
  @apply w-full mx-2 my-2 bg-white text-center flex justify-center items-center rounded-lg font-bold text-lg;
  min-height: 80px;
}

.button-controll {
  @apply w-full mx-2 my-2 text-center flex justify-center items-center rounded-lg font-bold text-lg;
  min-height: 40px;
}
</style>
