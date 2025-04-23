<script setup lang="ts">
import { type ToolbarOptions, VPdfViewer } from '@vue-pdf-viewer/viewer';
import pdfWorker from 'pdfjs-dist/build/pdf.worker?url';

const props = withDefaults(
  defineProps<{
    src: string;
    toolbarOptions?: Partial<ToolbarOptions> | false | null;
  }>(),
  {
    toolbarOptions: null,
  }
);
</script>

<template>
  <VPdfViewer v-bind="props" :worker-url="pdfWorker" />
</template>
