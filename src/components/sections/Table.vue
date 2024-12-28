<script lang="ts" setup>

// 表格数据
const tableDataT90 = [
{
    model: 'DiffWater',
    // params: '10 B',
    UCIQE: '0.609',
    UIQM: '2.991',
    Uranker: '1.850',
},
{
    model: 'DM_Underwater',
    // params: '30 B',
    UCIQE: '0.614',
    UIQM: '2.972',
    Uranker: '2.167',
},
{
    model: 'Osmosis',
    // params: '20 B',
    UCIQE: '0.640',
    UIQM: '2.844',
    Uranker: '1.916',

},
{
    model: 'CLIP_UIE',
    // params: '5 B',
    UCIQE: '0.619',
    UIQM: '2.892',
    Uranker: '2.323',

},
  {
    model: 'Our',
    // params: '5 B',
    UCIQE: '0.626',
    UIQM: '3.193',
    Uranker: '2.463',

},
]



const tableDataEUVP = [
{
    model: 'DiffWater',
    // params: '10 B',
    UCIQE: '0.614',
    UIQM: '2.916',
    Uranker: '2.085',
},
{
    model: 'DM_Underwater',
    // params: '30 B',
    UCIQE: '0.590',
    UIQM: '2.838',
    Uranker: '1.641',
},
{
    model: 'Osmosis',
    // params: '20 B',
    UCIQE: '0.637',
    UIQM: '2.637',
    Uranker: '2.091',

},
{
    model: 'CLIP_UIE',
    // params: '5 B',
    UCIQE: '0.625',
    UIQM: '2.818',
    Uranker: '2.510',

},
  {
    model: 'Our',
    // params: '5 B',
    UCIQE: '0.617',
    UIQM: '3.056',
    Uranker: '2.606',

},
]


const tableDataUCCS = [
{
    model: 'DiffWater',
    // params: '10 B',
    UCIQE: '0.554',
    UIQM: '2.985',
    Uranker: '0.900',
},
{
    model: 'DM_Underwater',
    // params: '30 B',
    UCIQE: '0.570',
    UIQM: '2.995',
    Uranker: '1.645',
},
{
    model: 'Osmosis',
    // params: '20 B',
    UCIQE: '0.626',
    UIQM: '2.938',
    Uranker: '1.508',

},
{
    model: 'CLIP_UIE',
    // params: '5 B',
    UCIQE: '0.568',
    UIQM: '2.971',
    Uranker: '1.464',

},
  {
    model: 'Our',
    // params: '5 B',
    UCIQE: '0.594',
    UIQM: '3.099',
    Uranker: '2.112',

},
]


const tableDataU45 = [
{
    model: 'DiffWater',
    // params: '10 B',
    UCIQE: '0.595',
    UIQM: '3.118',
    Uranker: '1.442',
},
{
    model: 'DM_Underwater',
    // params: '30 B',
    UCIQE: '0.603',
    UIQM: '3.107',
    Uranker: '1.810',
},
{
    model: 'Osmosis',
    // params: '20 B',
    UCIQE: '0.618',
    UIQM: '2.902',
    Uranker: '0.872',

},
{
    model: 'CLIP_UIE',
    // params: '5 B',
    UCIQE: '0.620',
    UIQM: '3.007',
    Uranker: '2.218',

},
  {
    model: 'Our',
    // params: '5 B',
    UCIQE: '0.621',
    UIQM: '3.213',
    Uranker: '2.230',

},
]



</script>

<template>
    <div>
        <el-divider />

        <el-row justify="center">
            <h1 class="section-title">More Results</h1>
        </el-row>
        
        <!-- 数据表格 -->
        <el-row justify="center">
            <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">

                <!-- 卡片 -->
                <el-card class="card">

                    <!-- 默认tab -->
                    <el-tabs class="demo-tabs" model-value="T90">

                    <!-- 第一个tab -->
                    <el-tab-pane label="T90" name="T90">

                        <!-- 表格数据 -->
                        <el-table 
                            :data="tableDataT90"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Model" width="100" sortable/>
<!--                            <el-table-column prop="params" label="#Params" min-width="120" sortable/>-->
                            <el-table-column prop="UCIQE" label="UCIQE" min-width="120" sortable/>
                            <el-table-column prop="UIQM" label="UIQM" min-width="120" sortable/>
                            <el-table-column prop="Uranker" label="Uranker" min-width="120" sortable/>

                        </el-table>
                    </el-tab-pane>

                    <!-- 第二个tab -->
                          <el-tab-pane label="EUVP" name="EUVP">

                        <!-- 表格数据 -->
                        <el-table
                            :data="tableDataEUVP"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Model" width="100" sortable/>
<!--                            <el-table-column prop="params" label="#Params" min-width="120" sortable/>-->
                            <el-table-column prop="UCIQE" label="UCIQE" min-width="120" sortable/>
                            <el-table-column prop="UIQM" label="UIQM" min-width="120" sortable/>
                            <el-table-column prop="Uranker" label="Uranker" min-width="120" sortable/>

                        </el-table>
                    </el-tab-pane>

                    <!-- 第三个tab -->
                          <el-tab-pane label="UCCS" name="UCCS">

                        <!-- 表格数据 -->
                        <el-table
                            :data="tableDataUCCS"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Model" width="100" sortable/>
<!--                            <el-table-column prop="params" label="#Params" min-width="120" sortable/>-->
                            <el-table-column prop="UCIQE" label="UCIQE" min-width="120" sortable/>
                            <el-table-column prop="UIQM" label="UIQM" min-width="120" sortable/>
                            <el-table-column prop="Uranker" label="Uranker" min-width="120" sortable/>

                        </el-table>
                    </el-tab-pane>

                    <!-- 第四个tab -->
                          <el-tab-pane label="U45" name="U45">

                        <!-- 表格数据 -->
                        <el-table
                            :data="tableDataU45"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Model" width="100" sortable/>
<!--                            <el-table-column prop="params" label="#Params" min-width="120" sortable/>-->
                            <el-table-column prop="UCIQE" label="UCIQE" min-width="120" sortable/>
                            <el-table-column prop="UIQM" label="UIQM" min-width="120" sortable/>
                            <el-table-column prop="Uranker" label="Uranker" min-width="120" sortable/>

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
  