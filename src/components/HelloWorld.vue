<script setup lang="ts">
import Header from "../commonents/Header/Header.vue";
import Aside from "../commonents/Aside/Aside.vue";
import Main from "../commonents/Main/Main.vue";

</script>

<template>
  <div class="common-layout">
    <el-container>
      <el-header class="Header">
        <Header></Header>
      </el-header>
      <el-container>
        <el-aside width="200px" class="Aside">
          <Aside></Aside>
        </el-aside>
        <el-main>
          <Main></Main>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>
<style scoped>
.common-layout {
  width: 100%;
  height: 100%;
}

.Header {
  background-color: #262626;
}

.el-main {
  height: 100%;
  padding: 0;
  background-color: #f5f5f5;
}

.el-container {
  height: 100%;
}

.Aside {
  background-color: #333333;
}
</style>
