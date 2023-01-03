<script setup lang="ts">
import { storageDemo } from "~/logic/storage";

function openOptionsPage() {
  browser.runtime.openOptionsPage();
}
const clickMe = () => {
  console.log("1");
};
</script>

<template>
  <main class="w-[300px] px-4 py-5 text-center text-gray-700">
    <Logo />
    <div>Popup</div>
    <SharedSubtitle />

    <button class="btn mt-2" @click="openOptionsPage">Open Options</button>
    <div class="mt-2">
      <span class="opacity-50">Storage:</span> {{ storageDemo }}
      <button type="button" class="btn mt-2" @click="clickMe">Click Me!</button>
    </div>
  </main>
</template>
