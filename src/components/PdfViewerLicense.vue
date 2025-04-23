<script setup lang="ts">
import { useLicense } from '@vue-pdf-viewer/viewer';
import { onBeforeMount } from 'vue';

const licenseKey = import.meta.env.VITE_VPV_LICENSE ?? 'YOUR_LICENSE_KEY';

onBeforeMount(() => {
  useLicense(licenseKey);
});
</script>

<template>
  <slot />
</template>
