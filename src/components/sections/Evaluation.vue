<script lang="ts" setup>

const tableData1 = [
  { model: 'Badrobot-CJ', dc_asr: 0.34, dc_hrs: 2.71, di_asr: 0.80, di_hrs: 5.27, wr_asr: 0.70, wr_hrs: 4.92, sd_asr: 0.45, sd_hrs: 3.63, ip_asr: 0.43, ip_hrs: 3.59, overall_asr: 0.56, overall_hrs: 4.00 },
  { model: 'Badrobot-CD', dc_asr: 0.23, dc_hrs: 2.09, di_asr: 0.43, di_hrs: 3.49, wr_asr: 0.44, wr_hrs: 3.42, sd_asr: 0.13, sd_hrs: 1.56, ip_asr: 0.19, ip_hrs: 2.42, overall_asr: 0.30, overall_hrs: 2.66 },
  { model: 'Badrobot-SM', dc_asr: 0.19, dc_hrs: 1.76, di_asr: 0.58, di_hrs: 3.89, wr_asr: 0.34, wr_hrs: 3.02, sd_asr: 0.13, sd_hrs: 1.38, ip_asr: 0.16, ip_hrs: 1.94, overall_asr: 0.34, overall_hrs: 2.61 },
  { model: 'RoboPAIR', dc_asr: 0.51, dc_hrs: 3.94, di_asr: 0.79, di_hrs: 5.42, wr_asr: 0.68, wr_hrs: 4.90, sd_asr: 0.50, sd_hrs: 4.22, ip_asr: 0.53, ip_hrs: 4.48, overall_asr: 0.63, overall_hrs: 4.64 },
  { model: 'Cipher', dc_asr: 0.63, dc_hrs: 4.95, di_asr: 0.83, di_hrs: 5.62, wr_asr: 0.66, wr_hrs: 4.97, sd_asr: 0.49, sd_hrs: 3.82, ip_asr: 0.52, ip_hrs: 4.94, overall_asr: 0.68, overall_hrs: 5.08 },
  { model: 'CodeChameleon', dc_asr: 0.52, dc_hrs: 4.28, di_asr: 0.62, di_hrs: 4.60, wr_asr: 0.44, wr_hrs: 3.48, sd_asr: 0.46, sd_hrs: 4.03, ip_asr: 0.51, ip_hrs: 4.28, overall_asr: 0.55, overall_hrs: 4.35 },
  { model: 'Deepinception', dc_asr: 0.28, dc_hrs: 2.34, di_asr: 0.60, di_hrs: 4.10, wr_asr: 0.42, wr_hrs: 3.58, sd_asr: 0.29, sd_hrs: 2.56, ip_asr: 0.24, ip_hrs: 2.48, overall_asr: 0.41, overall_hrs: 3.11 },
  { model: 'GCG', dc_asr: 0.11, dc_hrs: 1.22, di_asr: 0.40, di_hrs: 2.71, wr_asr: 0.25, wr_hrs: 2.01, sd_asr: 0.09, sd_hrs: 1.16, ip_asr: 0.12, ip_hrs: 1.53, overall_asr: 0.23, overall_hrs: 1.85 },
  { model: 'Gptfuzzer', dc_asr: 0.06, dc_hrs: 0.81, di_asr: 0.13, di_hrs: 1.37, wr_asr: 0.23, wr_hrs: 2.12, sd_asr: 0.07, sd_hrs: 0.94, ip_asr: 0.11, ip_hrs: 1.12, overall_asr: 0.10, overall_hrs: 1.13 },
  { model: 'ReNeLLM', dc_asr: 0.46, dc_hrs: 4.03, di_asr: 0.62, di_hrs: 4.53, wr_asr: 0.55, wr_hrs: 4.37, sd_asr: 0.36, sd_hrs: 3.44, ip_asr: 0.44, ip_hrs: 4.09, overall_asr: 0.51, overall_hrs: 4.18 },
  { model: 'ICA', dc_asr: 0.07, dc_hrs: 0.66, di_asr: 0.31, di_hrs: 1.89, wr_asr: 0.17, wr_hrs: 1.14, sd_asr: 0.03, sd_hrs: 0.49, ip_asr: 0.09, ip_hrs: 1.04, overall_asr: 0.17, overall_hrs: 1.18 },
  { model: 'MJP', dc_asr: 0.08, dc_hrs: 0.87, di_asr: 0.19, di_hrs: 1.36, wr_asr: 0.17, wr_hrs: 1.32, sd_asr: 0.07, sd_hrs: 0.77, ip_asr: 0.07, ip_hrs: 0.86, overall_asr: 0.12, overall_hrs: 1.08 },
  { model: 'Multilingual', dc_asr: 0.05, dc_hrs: 0.46, di_asr: 0.07, di_hrs: 0.57, wr_asr: 0.11, wr_hrs: 1.05, sd_asr: 0.04, sd_hrs: 0.58, ip_asr: 0.07, ip_hrs: 0.58, overall_asr: 0.06, overall_hrs: 0.55 },
  { model: 'SceneTAP', dc_asr: 0.13, dc_hrs: 1.74, di_asr: 0.58, di_hrs: 4.27, wr_asr: 0.12, wr_hrs: 1.50, sd_asr: 0.11, sd_hrs: 1.33, ip_asr: 0.29, ip_hrs: 4.00, overall_asr: 0.34, overall_hrs: 2.98 },
  { model: 'SceneTAP-Adapted', dc_asr: 0.24, dc_hrs: 2.76, di_asr: 0.74, di_hrs: 5.39, wr_asr: 0.33, wr_hrs: 4.00, sd_asr: 0.01, sd_hrs: 0.50, ip_asr: 0.17, ip_hrs: 4.67, overall_asr: 0.45, overall_hrs: 3.98},
  { model: 'Vanilla', dc_asr: 0.15, dc_hrs: 1.40, di_asr: 0.52, di_hrs: 3.49, wr_asr: 0.29, wr_hrs: 2.69, sd_asr: 0.11, sd_hrs: 1.21, ip_asr: 0.13, ip_hrs: 1.71, overall_asr: 0.29, overall_hrs: 2.27 },
  { model: 'Shawshank-Vanilla', dc_asr: 0.51, dc_hrs: 4.40, di_asr: 0.75, di_hrs: 5.41, wr_asr: 0.66, wr_hrs: 5.17, sd_asr: 0.39, sd_hrs: 3.61, ip_asr: 0.33, ip_hrs: 3.72, overall_asr: 0.57, overall_hrs: 4.64 },
  { model: 'Shawshank', dc_asr: 0.77, dc_hrs: 6.68, di_asr: 0.84, di_hrs: 6.19, wr_asr: 0.77, wr_hrs: 5.98, sd_asr: 0.58, sd_hrs: 5.35, ip_asr: 0.54, ip_hrs: 5.18, overall_asr: 0.75, overall_hrs: 6.13 },
]

const tableData2 = [
  { model: 'GPT-4o', dc_asr: 0.50, dc_hrs: 4.17, di_asr: 0.74, di_hrs: 5.02, wr_asr: 0.69, wr_hrs: 4.92, sd_asr: 0.44, sd_hrs: 3.82, ip_asr: 0.43, ip_hrs: 3.97, overall_asr: 0.59, overall_hrs: 4.47 },
  { model: 'GPT-5.5', dc_asr: 0.42, dc_hrs: 4.23, di_asr: 0.62, di_hrs: 4.49, wr_asr: 0.25, wr_hrs: 1.75, sd_asr: 0.22, sd_hrs: 2.22, ip_asr: 0.57, ip_hrs: 5.00, overall_asr: 0.49, overall_hrs: 4.02 },
  { model: 'Qwen3-VL', dc_asr: 0.77, dc_hrs: 6.68, di_asr: 0.84, di_hrs: 6.19, wr_asr: 0.77, wr_hrs: 5.98, sd_asr: 0.58, sd_hrs: 5.35, ip_asr: 0.54, ip_hrs: 5.18, overall_asr: 0.75, overall_hrs: 6.13 },
  { model: 'Qwen3-VL', dc_asr: 0.61, dc_hrs: 4.65, di_asr: 0.80, di_hrs: 6.51, wr_asr: 0.38, wr_hrs: 5.50, sd_asr: 0.22, sd_hrs: 4.44, ip_asr: 0.57, ip_hrs: 5.29, overall_asr: 0.64, overall_hrs: 5.58 },
  { model: 'Gemini-2.0', dc_asr: 0.62, dc_hrs: 5.42, di_asr: 0.69, di_hrs: 5.02, wr_asr: 0.32, wr_hrs: 3.13, sd_asr: 0.34, sd_hrs: 3.37, ip_asr: 0.24, ip_hrs: 3.01, overall_asr: 0.56, overall_hrs: 4.66 },
  { model: 'Gemini-3.1', dc_asr: 0.39, dc_hrs: 2.81, di_asr: 0.56, di_hrs: 4.22, wr_asr: 0.12, wr_hrs: 1.62, sd_asr: 0.11, sd_hrs: 1.67, ip_asr: 0.14, ip_hrs: 4.14, overall_asr: 0.40, overall_hrs: 3.34 },
  { model: 'GLM-4.5', dc_asr: 0.28, dc_hrs: 3.62, di_asr: 0.35, di_hrs: 3.39, wr_asr: 0.37, wr_hrs: 4.85, sd_asr: 0.26, sd_hrs: 2.90, ip_asr: 0.18, ip_hrs: 2.77, overall_asr: 0.30, overall_hrs: 3.36 },
  { model: 'Claude-3.5', dc_asr: 0.15, dc_hrs: 1.99, di_asr: 0.28, di_hrs: 2.54, wr_asr: 0.22, wr_hrs: 2.86, sd_asr: 0.21, sd_hrs: 2.56, ip_asr: 0.17, ip_hrs: 2.44, overall_asr: 0.21, overall_hrs: 2.36 },
  { model: 'Deepseek-VL2', dc_asr: 0.32, dc_hrs: 3.32, di_asr: 0.34, di_hrs: 3.14, wr_asr: 0.37, wr_hrs: 3.43, sd_asr: 0.22, sd_hrs: 2.49, ip_asr: 0.30, ip_hrs: 3.26, overall_asr: 0.32, overall_hrs: 3.15 },
]

const tableData3 = [
  { model: 'GPT-4o', simple_psr_init: 0.66, simple_psr_atk: 0.15, medium_psr_init: 0.52, medium_psr_atk: 0.08, complex_psr_init: 0.41, complex_psr_atk: 0.15, overall_psr_init: 0.53, overall_psr_atk: 0.13, drop: '56.60%' },
  { model: 'Qwen3-VL', simple_psr_init: 0.65, simple_psr_atk: 0.20, medium_psr_init: 0.58, medium_psr_atk: 0.07, complex_psr_init: 0.57, complex_psr_atk: 0.15, overall_psr_init: 0.60, overall_psr_atk: 0.14, drop: '76.67%' },
  { model: 'Gemini-2.0', simple_psr_init: 0.44, simple_psr_atk: 0.27, medium_psr_init: 0.19, medium_psr_atk: 0.06, complex_psr_init: 0.12, complex_psr_atk: 0.05, overall_psr_init: 0.25, overall_psr_atk: 0.12, drop: '52.00%' },
  { model: 'GLM-4.5', simple_psr_init: 0.42, simple_psr_atk: 0.32, medium_psr_init: 0.22, medium_psr_atk: 0.13, complex_psr_init: 0.05, complex_psr_atk: 0.05, overall_psr_init: 0.23, overall_psr_atk: 0.17, drop: '26.08%' },
  { model: 'Claude-3.5', simple_psr_init: 0.43, simple_psr_atk: 0.25, medium_psr_init: 0.16, medium_psr_atk: 0.17, complex_psr_init: 0.07, complex_psr_atk: 0.02, overall_psr_init: 0.22, overall_psr_atk: 0.14, drop: '36.36%' },
  { model: 'Deepseek-VL2', simple_psr_init: 0.16, simple_psr_atk: 0.13, medium_psr_init: 0.13, medium_psr_atk: 0.10, complex_psr_init: 0.06, complex_psr_atk: 0.06, overall_psr_init: 0.12, overall_psr_atk: 0.10, drop: '16.67%' }
]

const tableData4 = [
  { model: 'BadRobot-CJ', qwen3guard_asr: 0.26, qwen3guard_hrs: 0.55, sap_asr: 0.58, sap_hrs: 0.13 },
  { model: 'RoboPAIR', qwen3guard_asr: 0.43, qwen3guard_hrs: 0.57, sap_asr: 0.57, sap_hrs: 0.10 },
  { model: 'Cipher', qwen3guard_asr: 0.49, qwen3guard_hrs: 0.45, sap_asr: 0.16, sap_hrs: 0.44 },
  { model: 'CodeChameleon', qwen3guard_asr: 0.26, qwen3guard_hrs: 0.50, sap_asr: 0.04, sap_hrs: 0.12 },
  { model: 'ReNeLLM', qwen3guard_asr: 0.29, qwen3guard_hrs: 0.35, sap_asr: 0.16, sap_hrs: 0.13 },
  { model: 'Shawshank-Vanilla', qwen3guard_asr: 0.18, qwen3guard_hrs: 0.37, sap_asr: 0.27, sap_hrs: 0.29 },
  { model: 'Shawshank', qwen3guard_asr: 0.52, qwen3guard_hrs: 0.65, sap_asr: 0.59, sap_hrs: 0.52 }
]


</script>

<template>
    <div>
        <el-divider />

        <el-row justify="center">
            <h1 class="section-title">Evaluation</h1>
        </el-row>
        
        <el-row justify="center">
            <el-col :xs="24" :sm="20" :md="16" :lg="18" :xl="12">
                <el-card class="card">
                    <el-tabs class="demo-tabs" model-value="Method A">
                    <el-tab-pane label="Comparison of Baselines" name="Method A">

                        <el-table :data="tableData1" style="width: 100%">
                            <el-table-column fixed prop="model" label="Method" sortable align="center" width="150"/>
                            <el-table-column prop="dc_asr" label="DC-ASR" sortable align="center"/>
                            <el-table-column prop="dc_hrs" label="DC-HRS" sortable align="center"/>
                            <el-table-column prop="di_asr" label="DI-ASR" sortable align="center"/>
                            <el-table-column prop="di_hrs" label="DI-HRS" sortable align="center"/>
                            <el-table-column prop="wr_asr" label="WR-ASR" sortable align="center"/>
                            <el-table-column prop="wr_hrs" label="WR-HRS" sortable align="center"/>
                            <el-table-column prop="sd_asr" label="SD-ASR" sortable align="center"/>
                            <el-table-column prop="sd_hrs" label="SD-HRS" sortable align="center"/>
                            <el-table-column prop="ip_asr" label="IP-ASR" sortable align="center"/>
                            <el-table-column prop="ip_hrs" label="IP-HRS" sortable align="center"/>
                            <el-table-column prop="overall_asr" label="Overall-ASR" width="60" sortable align="center"/>
                            <el-table-column prop="overall_hrs" label="Overall-HRS" width="60" sortable align="center"/>
                        </el-table>
                    </el-tab-pane>

                    <el-tab-pane label="Jailbreak Attacks" name="Method B">
                        <el-table :data="tableData2" style="width: 100%">
                            <el-table-column fixed prop="model" label="Model" sortable align="center"/>
                            <el-table-column prop="dc_asr" label="DC-ASR" sortable align="center"/>
                            <el-table-column prop="dc_hrs" label="DC-HRS" sortable align="center"/>
                            <el-table-column prop="di_asr" label="DI-ASR" sortable align="center"/>
                            <el-table-column prop="di_hrs" label="DI-HRS" sortable align="center"/>
                            <el-table-column prop="wr_asr" label="WR-ASR" sortable align="center"/>
                            <el-table-column prop="wr_hrs" label="WR-HRS" sortable align="center"/>
                            <el-table-column prop="sd_asr" label="SD-ASR" sortable align="center"/>
                            <el-table-column prop="sd_hrs" label="SD-HRS" sortable align="center"/>
                            <el-table-column prop="ip_asr" label="IP-ASR" sortable align="center"/>
                            <el-table-column prop="ip_hrs" label="IP-HRS" sortable align="center"/>
                            <el-table-column prop="overall_asr" label="Overall-ASR" width="30" sortable align="center"/>
                            <el-table-column prop="overall_hrs" label="Overall-HRS" width="30" sortable align="center"/>
                        </el-table>
                    </el-tab-pane>

                    <el-tab-pane label="DoS Attacks" name="Method C">
                        <el-table :data="tableData3" style="width: 100%">
                            <el-table-column fixed prop="model" label="Model"  sortable align="center"/>
                            <el-table-column prop="simple_psr_init" label="Simple PSR-init" sortable align="center"/>
                            <el-table-column prop="simple_psr_atk" label="Simple PSR-atk" sortable align="center"/>
                            <el-table-column prop="medium_psr_init" label="Medium PSR-init" sortable align="center"/>
                            <el-table-column prop="medium_psr_atk" label="Medium PSR-atk" sortable align="center"/>
                            <el-table-column prop="complex_psr_init" label="Complex PSR-init" sortable align="center"/>
                            <el-table-column prop="complex_psr_atk" label="Complex PSR-atk" sortable align="center"/>
                            <el-table-column prop="overall_psr_init" label="Overall PSR-init" sortable align="center"/>
                            <el-table-column prop="overall_psr_atk" label="Overall PSR-atk" sortable align="center"/>
                            <el-table-column prop="drop" label="Drop" sortable align="center"/>
                        </el-table>
                    </el-tab-pane>

                    <el-tab-pane label="Defenses" name="Method D">
                        <el-table :data="tableData4" style="width: 100%">
                            <el-table-column fixed prop="model" label="Method"  sortable align="center"/>
                            <el-table-column prop="qwen3guard_asr" label="Qwen3Guard" sortable align="center"/>
                            <el-table-column prop="qwen3guard_hrs" label="SAP" sortable align="center"/>
                            <el-table-column prop="sap_asr" label="Llama-Guard-4-12B" sortable align="center"/>
                            <el-table-column prop="sap_hrs" label="WildGuard" sortable align="center"/>
                        </el-table>
                    </el-tab-pane>
                    </el-tabs>

                </el-card>
            </el-col>
        </el-row>

    </div>
</template>

<style scoped>
.card {
    margin-top: 20px;
}
</style>

