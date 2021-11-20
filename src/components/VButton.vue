<template>
  <button @click="onClick">{{ text }}</button>
</template>

<script lang="ts">
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  methods: {
    onClick(e: unknown) {
      console.log(this.text);

      this.$emit("my-event", e);
    },
  },
});
</script>
