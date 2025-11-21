<script lang="ts" setup>

import { ElIcon } from 'element-plus'
import { HomeFilled, SuccessFilled } from '@element-plus/icons-vue'

const home = {
    name: "",
    link: "",
}

const logo = {
    name: "",
    link: "",
}

const more_paper = {
    "ExtDM": {
        name: "",
        link: "",
    },
    "MPOT": {
        name: "",
        link: "",
    },
    "ControlNet": {
        name: "",
        link: "",
    }
}


</script>

<template>

    <el-affix :offset="0" :style="{width: '100%'}">
    
    </el-affix>
</template>

<style>

.el-menu {
	background: none;
}

.el-menu--popup {
	min-width: 100%;
}

.el-affix--fixed {
	box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
	background-image: radial-gradient(#ffffffca 1px,#ffffff 1px);
	background-size: 3px 3px;
}

.el-header {
    --el-header-height: 50px;
}

</style>

<style scoped>

.el-menu--horizontal > .el-menu-item:nth-child(2) {
    margin-right: auto;
}

.el-menu--horizontal {
    --el-menu-horizontal-height: 50px;
}

a:hover {
  color: inherit;
  border-bottom: none;
}

a {
	text-decoration: None;
	color: inherit;
}

</style>

  
