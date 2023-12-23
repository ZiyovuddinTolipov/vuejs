<template>
  <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

  <div class="bg-slate-900 min-h-[100vh] flex justify-center items-center text-slate-300">
    <div class="bg-slate-700 max-w-[600px] w-full min-h-[300px] rounded-[16px] mx-4 relative flex flex-col gap-2">
      <h1 class="text-3xl font-bol uppercase text-center pt-4">
        Counter App
      </h1>
      <h3 class="text-center text-2xl uppercase font-semibold">Counter: {{ counter }}</h3>
      <div class="w-100 flex justify-center items-center gap-2 text-xl font-semibold uppercase">
        <button class="bg-blue-500 text-white py-1 px-3 rounded-md" @click="onIncrement">ADD</button>
        <button class="bg-red-500 text-white py-1 px-3 rounded-md" @click="onDecrement">DELETE</button>
      </div>
      <p class="absolute text-center w-full bottom-2 text-red-200">! MAX=12 MIN=0</p>
    </div>

  </div>
</template>

<script >
export default {
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    onIncrement() {
      if (this.counter < 12) {
        this.counter += 1
      }
    },
    onDecrement() {
      if (this.counter > 0) {
        this.counter -= 1;
      }
    }
  }
}
</script>
<style scoped></style>
