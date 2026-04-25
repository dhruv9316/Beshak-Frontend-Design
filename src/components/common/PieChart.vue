<template>
  <VChart class="h-[360px] w-[360px]" :option="chartOption" autoresize />
</template>

<script setup lang="ts">
import { computed } from "vue";
import VChart from "vue-echarts";
import { use } from "echarts/core";
import { CanvasRenderer } from "echarts/renderers";
import { PieChart } from "echarts/charts";
import { TooltipComponent } from "echarts/components";

use([CanvasRenderer, PieChart, TooltipComponent]);

const chartOption = computed(() => ({
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
      data: [
        {
          value: 28,
          name: "Stable Assets",
          itemStyle: { color: "#FACC15" },
          label: {
            show: true,
            position: "inside",
            color: "#111827",
            formatter:
              "{percent|28%}\n{title|Stable Assets}\n{sub|GSPs, FDs, Bonds}",
            rich: {
              percent: { fontSize: 20, fontWeight: 700, lineHeight: 30 },
              title: { fontSize: 12, fontWeight: 700, lineHeight: 22 },
              sub: { fontSize: 10, fontWeight: 500, lineHeight: 16 },
            },
          },
        },
        {
          value: 72,
          name: "Equity Investment",
          itemStyle: { color: "#4AC37A" },
          label: {
            show: true,
            position: "inside",
            color: "#FFFFFF",
            formatter:
              "{percent|72%}\n{title|Equity Investment}\n{sub|Stocks, MFs, Crypto}",
            rich: {
              percent: { fontSize: 20, fontWeight: 700, lineHeight: 30 },
              title: { fontSize: 12, fontWeight: 700, lineHeight: 22 },
              sub: { fontSize: 10, fontWeight: 500, lineHeight: 16 },
            },
          },
        },
      ],
    },
  ],
}));
</script>
