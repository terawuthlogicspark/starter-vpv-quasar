<script setup lang="ts">
import { VPdfViewer, ToolbarOptions } from '@vue-pdf-viewer/viewer';
import pdfWorker from 'pdfjs-dist/build/pdf.worker?url';

const props = withDefaults(
  defineProps<{
    src: string;
    toolbarOptions?: Partial<ToolbarOptions> | false;
  }>(),
  {
    src: '',
    toolbarOptions: false,
  }
);
// const licenseKey = import.meta.env.VITE_VPV_LICENSE ?? 'your-VPV-license-key';
// useLicense({ licenseKey });
</script>

<template>
  <VPdfViewer v-bind="props" :worker-url="pdfWorker" />
</template>
