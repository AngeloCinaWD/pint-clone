<template>
  <div @mouseenter="hover = true" @mouseleave="hover = false" class="relative">
    <img :src="src" alt="" class="rounded-lg" />
    <div
      v-if="hover"
      class="absolute bg-dark inset-0 opacity-50 w-full h-full rounded-lg"
    ></div>
    <div
      v-if="hover"
      class="absolute top-0 w-full h-full flex flex-col justify-between p-3"
    >
      <div class="flex items-center justify-between">
        <button
          class="flex items-center justify-center"
          type="button"
          name="button"
        >
          <p class="font-semibold text-white">{{ board }}</p>
          <span class="material-icons text-white">expand_more</span>
        </button>

        <button
          class="text-white bg-primary rounded-full px-5 py-3"
          type="button"
          name="button"
        >
          Save
        </button>
      </div>

      <div class="flex items-center justify-end">
        <button
          class="mr-2 flex items-center justify-center bg-white rounded-full p-2 opacity-75 hover:opacity-100"
          type="button"
          name="button"
        >
          <span class="material-icons">ios_share</span>
        </button>

        <button
          class="flex items-center justify-center bg-white rounded-full p-2 opacity-75 hover:opacity-100"
          type="button"
          name="button"
        >
          <span class="material-icons">more_horiz</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['src', 'board'],
  data() {
    return {
      hover: false,
    };
  },
};
</script>
