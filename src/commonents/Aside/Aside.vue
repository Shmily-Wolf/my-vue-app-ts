<template>
    <div></div>
    <el-row class="tac">
        <el-col>
            <el-radio-group v-model="isCollapse" style="margin-bottom: 20px">
                <el-radio-button :label="false">expand</el-radio-button>
                <el-radio-button :label="true">collapse</el-radio-button>
            </el-radio-group>
            <el-menu active-text-color="#ffd04b" background-color="#333333" class="el-menu-vertical-demo"
                default-active="2" text-color="#fff" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
                <el-sub-menu index="1">
                    <template #title>
                        <el-icon>
                            <location />
                        </el-icon>
                        <span>Navigator One</span>
                    </template>
                    <el-menu-item-group title="Group One">
                        <el-menu-item index="1-1">item one</el-menu-item>
                        <el-menu-item index="1-2">item two</el-menu-item>
                    </el-menu-item-group>
                    <el-menu-item-group title="Group Two">
                        <el-menu-item index="1-3">item three</el-menu-item>
                    </el-menu-item-group>
                    <el-sub-menu index="1-4">
                        <template #title>item four</template>
                        <el-menu-item index="1-4-1">item one</el-menu-item>
                    </el-sub-menu>
                </el-sub-menu>
                <el-menu-item index="2">
                    <el-icon>
                        <icon-menu />
                    </el-icon>
                    <span>Navigator Two</span>
                </el-menu-item>
                <el-menu-item index="3">
                    <el-icon>
                        <document />
                    </el-icon>
                    <span>Navigator Three</span>
                </el-menu-item>
                <el-menu-item index="4">
                    <el-icon>
                        <setting />
                    </el-icon>
                    <span>Navigator Four</span>
                </el-menu-item>
            </el-menu>
        </el-col>
    </el-row>
</template>

<script setup lang="ts">
import {
    Document,
    Menu as IconMenu,
    Location,
    Setting
} from '@element-plus/icons-vue'
import { ref } from 'vue';
const handleOpen = (key: string, keyPath: string[]) => {
    console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
    console.log(key, keyPath)
}
const isCollapse = ref(false)
</script>

<style scoped lang="less">
.el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
}

.el-menu {
    border-right: 1px solid #333;
}
</style>