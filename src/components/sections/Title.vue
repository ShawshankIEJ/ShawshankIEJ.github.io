<script lang="ts" setup>

import { ElIcon } from 'element-plus'
import { Document, Files, MagicStick, Picture, DataAnalysis, Film } from '@element-plus/icons-vue'


const logo = ''


const title = 'The Shawshank Redemption of Embodied AI: Understanding and Benchmarking Indirect Environmental Jailbreaks'


const title_color = '#000000'

const title_supp = ''


const title_supp_color = '#42B883'


const btn_color = '#444444'


const authors = [
  // {
  //   name: "Your Name",
  //   icon: "",
  //   homepage: "",
  //   address_flag: "1,#"
  // },
]


const addresses = []


const con_and_corresponding_author = ""
  // "#: Equal Contribution. *: Corresponding Author."


const news = ""


const emphases = [
  "Warning: This paper contains potentially harmful AI-generated language and aggressive actions!"
]


const buttons = []

</script>

<template>
  <div>

    <el-row v-if="logo" justify="center">
      <el-image :src="logo" class="logo" fit="cover" />
    </el-row>


    <el-row justify="center">
      <el-col :span="20">
        <h1 class="paper-title">
          <span v-if="title" :style="{color:title_color}"> {{ title }}</span>
          <span v-if="title_supp" :style="{color:title_supp_color}"> {{ title_supp }}</span>
        </h1>
      </el-col>
    </el-row>




    <el-row justify="center" class="emphasis" v-for="emphasis in emphases">
        {{ emphasis }}
    </el-row>



  </div>
</template>

<style scoped>


.paper-title {
  font-family: "MyFont", Verdana, sans-serif;
  letter-spacing: 2px;
  font-size: 42px;
  margin: 32px;
  text-align: center;
}



.emphasis {
  color: red;
  font-weight: bold;
  margin: 8px;
  font-size: 22px;
  text-align: center;
}


.btn-text {
  font-size: 18px;
  color: #ffffff;
}

.el-alert {
  margin: 10px 0 0;
}

.el-alert:first-child {
  margin: 0;
}

/* .logo {
  width: 150px; 
  height: 150px;
  border-radius: 50%;
  box-shadow: #ced3dc 0px 0px 3px 2px;
  margin-top: 40px;
} */


a:-webkit-any-link {
  text-decoration: none;
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
