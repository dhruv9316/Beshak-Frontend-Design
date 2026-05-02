<template>
  <VChart class="h-full w-full" :option="chartOption" autoresize />
</template>

<script setup lang="ts">
import { computed } from "vue";
import VChart from "vue-echarts";
import { use } from "echarts/core";
import { CanvasRenderer } from "echarts/renderers";
import { PieChart } from "echarts/charts";
import { TooltipComponent } from "echarts/components";

const props = defineProps<{
  options: {
    name: string;
    value: number;
    label: string;
  }[];
}>();

use([CanvasRenderer, PieChart, TooltipComponent]);

// Can replace with random colors or props colors later
const colors = [
  {
    color: "#FACC15",
    labelColor: "#111827",
  },
  {
    color: "#4AC37A",
    labelColor: "#FFFFFF",
  },
];

const chartOption = computed(() => {
  const optionsData = props.options.map(({ name, label, value }, index) => ({
    value,
    name,
    itemStyle: { color: colors[index].color },
    label: {
      show: true,
      position: "inside",
      color: colors[index].labelColor,
      formatter: `{percent|${value}%}\n{title|${name}}\n{sub|${label}}`,
      rich: {
        percent: { fontSize: 20, fontWeight: 700, lineHeight: 30 },
        title: { fontSize: 12, fontWeight: 700, lineHeight: 22 },
        sub: { fontSize: 10, fontWeight: 500, lineHeight: 16 },
      },
    },
  }));

  return {
    animation: false,
    tooltip: { trigger: "item", formatter: "{b}: {c}%" },
    series: [
      {
        type: "pie",
        radius: "88%",
        center: ["50%", "50%"],
        startAngle: 0,
        clockwise: false,
        avoidLabelOverlap: false,
        labelLine: { show: false },
        itemStyle: { borderWidth: 0 },
        data: optionsData,
      },
    ],
  };
});
</script>
