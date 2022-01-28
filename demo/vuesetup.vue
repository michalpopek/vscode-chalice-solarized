<script setup>
import { ref, computed } from "vue";
import HelloWorld from "@/components/HelloWorld.vue";
const shouldGreet = ref(true);
const props = defineProps({
  name: {
    type: String,
    default: false,
    required: true,
  },
});
const greeting = computed(() => `Hello, ${props.name}`);
</script>

<template>
  <main>
    <HelloWorld v-if="shouldGreet" :greeting="greeting" />
  </main>
</template>

<style scoped>
main {
  display: flex;
  justify-content: center;
}
</style>
