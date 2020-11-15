<template>
  <div class="w-full h-screen flex justify-center content-center bg-green-200">
    <div class="flex rounded-lg bg-gray-700 w-10/12 md:mx-0 md:w-6/12 mt-24 py-32 border border-gray-400 justify-center flex-col items-center" style="max-height:600px">
      <!-- Display -->
      <div class="w-10/12 bg-gray-200 my-4 flex justify-end rounded-lg" style="min-height: 70px">
        <span class="uppercase font-bold text-xl">Teste</span>
      </div>
      <!-- Keyboards -->
      <div class="w-10/12 h-full  mb-4">
        <div class="row flex justify-center">
          <div class="button">
            7
          </div>
          <div class="button">
            8
          </div>
          <div class="button">
            9
          </div>
          <div class="button">
            /
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button">
            4
          </div>
          <div class="button">
            5
          </div>
          <div class="button">
            6
          </div>
          <div class="button">
            X
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button">
            1
          </div>
          <div class="button">
            2
          </div>
          <div class="button">
            3
          </div>
          <div class="button">
            -
          </div>
        </div>
        <div class="row flex justify-center">
          <div class="button">
            0
          </div>
          <div class="button">
            .
          </div>
          <div class="button">
            +
          </div>
          <div class="button">
            =
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {};
</script>

<style>
.button {
  @apply w-full mx-2 my-2 bg-white text-center flex justify-center items-center rounded-lg font-bold text-lg;
  min-height: 80px;
}
</style>
