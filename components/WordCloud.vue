<script setup lang="ts">
import { onMounted, ref, watch } from "vue";
import B2wordcloud from "b2wordcloud";

const chartRef = ref<HTMLElement | null>(null);
const wordCloud = ref(null);

const initChart = () => {
  chartRef.value &&
    (wordCloud.value = new B2wordcloud(chartRef.value, {
      list: [
        ["夸克", 36],
        ["豆包", 62],
        ["纳米", 22],
        ["360", 36],
        ["秘塔", 46],
        ["天工", 36],
        ["心流", 62],
        ["百度", 22],
        ["博查", 36],
        ["知乎直答", 46],
        ["链企", 36],
        ["开搜", 62],
        ["问问小宇宙", 22],
        ["卡奥斯智能交互引擎", 36],
        ["Suppr 超能文献", 46],
        ["知料觅得", 36],
        ["Perplexity", 62],
        ["Genspark", 22],
        ["You.com", 36],
        ["Phind", 46],
        ["Andi Search", 36],
        ["Consensus", 62],
        ["Flowith", 22],
        ["Devv", 36],
        ["ChatGPT", 46],
        ["AMiner", 36],
        ["Lumina", 62],
        ["Felo", 22],
        ["Reddo", 36],
        ["Exa AI", 46],
        ["Dexa AI", 36],
        ["XAnswer", 62],
        ["Globe Explorer", 22],
        ["Reportify", 36],
        ["iAsk AI", 46],
        ["Komo Search", 36],
        ["Songtell", 62],
        ["ThinkAny", 22],
        ["Miku", 36],
        ["BiLin", 46],
        ["Scite", 40],
        ["Accio", 36],
        ["Wolfram Alpha", 20],
        ["Elicit", 44],
        ["Lepton Search", 62],
      ],
      tooltip: {
        show: true,
        formatter: function (item) {
          return "<div>" + item[0] + "</div>" + "<div>" + item[1] + "</div>";
        },
      },
      shadowColor: "rgba(0,0,0,0.9)",
      shadowOffsetX: 2,
      shadowOffsetY: 2,
      shadowBlur: 5,
      color: [
        ["#ed6e6c", "#f29038"],
        "#ed6e6c",
        "#ace437",
        "#e3e8f0",
        "#3aa4ee",
        ["#3aa4ee", "#fff"],
      ],
    }));
};

onMounted(() => {
  initChart();
});
</script>

<template>
  <div ref="chartRef" class="chart"></div>
</template>

<style scoped>
.chart {
  width: 300px;
  height: 300px;
  :deep(canvas) {
    background-color: transparent !important;
  }
}
</style>
