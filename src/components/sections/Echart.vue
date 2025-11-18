<script>
import { use } from 'echarts/core';
import { CanvasRenderer } from 'echarts/renderers';
import { RadarChart } from 'echarts/charts';
import {
  TitleComponent,
  TooltipComponent,
  LegendComponent,
} from 'echarts/components';
import VChart from 'vue-echarts';
import { ref, provide } from 'vue';

use([CanvasRenderer, RadarChart, TitleComponent, TooltipComponent, LegendComponent]);

export default {
  components: {
    VChart,
  },
  setup() {
    provide('THEME_KEY', 'light');
  },
  data() {
    return {
      option: {
        title: {
          text: 'Model Performance Radar Chart',
        },
        legend: {
          data: [
            'Badrobot-CJ', 'Badrobot-CD', 'Badrobot-SM', 'RoboPAIR', 'Cipher', 'CodeChameleon', 
            'Deepinception', 'GCG', 'Gptfuzzer', 'ReNeLLM', 'ICA', 'MJP', 'Multilingual', 'Vanilla', 
            'Shawshank-Vanilla', 'Shawshank'
          ],
        },
        radar: {
          indicator: [
            { name: 'Damage Creatures', max: 1 },
            { name: 'Destroy Items', max: 1 },
            { name: 'Waste Resources', max: 1 },
            { name: 'Self-Destruction', max: 1 },
            { name: 'Invasion Privacy', max: 1 },
          ],
        },
        series: [
          {
            name: 'Model Performance',
            type: 'radar',
            data: [
              {
                value: [0.34, 0.80, 0.70, 0.45, 0.43],
                name: 'Badrobot-CJ',
                itemStyle: { color: '#FF6347' },
              },
              {
                value: [0.23, 0.43, 0.44, 0.13, 0.19],
                name: 'Badrobot-CD',
                itemStyle: { color: '#1E90FF' },
              },
              {
                value: [0.19, 0.58, 0.34, 0.13, 0.16],
                name: 'Badrobot-SM',
                itemStyle: { color: '#32CD32' },
              },
              {
                value: [0.51, 0.79, 0.68, 0.50, 0.53],
                name: 'RoboPAIR',
                itemStyle: { color: '#FFD700' },
              },
              {
                value: [0.63, 0.83, 0.66, 0.49, 0.52],
                name: 'Cipher',
                itemStyle: { color: '#8A2BE2' },
              },
              {
                value: [0.52, 0.62, 0.44, 0.46, 0.51],
                name: 'CodeChameleon',
                itemStyle: { color: '#FF8C00' },
              },
              {
                value: [0.28, 0.60, 0.42, 0.29, 0.24],
                name: 'Deepinception',
                itemStyle: { color: '#20B2AA' },
              },
              {
                value: [0.11, 0.40, 0.25, 0.09, 0.12],
                name: 'GCG',
                itemStyle: { color: '#D2691E' },
              },
              {
                value: [0.06, 0.13, 0.23, 0.07, 0.11],
                name: 'Gptfuzzer',
                itemStyle: { color: '#2E8B57' },
              },
              {
                value: [0.46, 0.62, 0.55, 0.36, 0.44],
                name: 'ReNeLLM',
                itemStyle: { color: '#FF1493' },
              },
              {
                value: [0.07, 0.31, 0.17, 0.03, 0.09],
                name: 'ICA',
                itemStyle: { color: '#8B0000' },
              },
              {
                value: [0.08, 0.19, 0.17, 0.07, 0.07],
                name: 'MJP',
                itemStyle: { color: '#4682B4' },
              },
              {
                value: [0.05, 0.07, 0.11, 0.04, 0.07],
                name: 'Multilingual',
                itemStyle: { color: '#6A5ACD' },
              },
              {
                value: [0.15, 0.52, 0.29, 0.11, 0.13],
                name: 'Vanilla',
                itemStyle: { color: '#ADFF2F' },
              },
              {
                value: [0.51, 0.75, 0.66, 0.39, 0.33],
                name: 'Shawshank-Vanilla',
                itemStyle: { color: '#FF4500' },
              },
              {
                value: [0.77, 0.84, 0.77, 0.58, 0.54],
                name: 'Shawshank',
                itemStyle: { color: '#FF0000' },
              },
            ],
          },
        ],
      },
    };
  },
};
</script>

<template>
  <div>
    <el-divider />
    <el-row justify="center">
      <h1 class="section-title">Benchmark Comparison</h1>
    </el-row>

    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
        <v-chart class="chart" :option="option" autoresize />
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.chart {
  height: 400px;
  margin-top: 20px;
}
</style>
