<template>
  <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

  <div class="bg-slate-900 min-h-[100vh] flex justify-center items-center text-slate-300">
    <div class="bg-slate-700 max-w-[600px] w-full min-h-[300px] rounded-[16px]">
      <h1 class="text-3xl font-bol uppercase text-center pt-4">
        Counter App
      </h1>
      <h3 class="text-center text-2xl uppercase font-semibold">Counter: {{ counter }}</h3>
      <div class="w-100 flex justify-center items-center gap-2">
        <button class="btn btn-success" @click="onIncrement">ADD</button>
      <button class="btn btn-danger" @:click="onDecrement">Delete</button>
      </div>
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
