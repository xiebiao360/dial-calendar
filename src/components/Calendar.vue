<template>
  <div id="container"></div>
</template>
<script lang="ts">
import { defineComponent, onMounted } from '@vue/runtime-core';
import { Canvas, Circle } from '@antv/g';
import { Renderer } from '@antv/g-canvas';

export default defineComponent({
  setup(prop) {
    onMounted(() => {
      const canvas = new Canvas({
        container: 'container',
        width: 600,
        height: 500,
        renderer: new Renderer(),
      });
      const circle = new Circle({
        style: {
          r: 50,
          fill: '#1890FF',
          stroke: '#F04864',
          lineWidth: 4,
          cursor: 'pointer',
        },
      });
      canvas.appendChild(circle);
      return {};
    });
  },
});
</script>
