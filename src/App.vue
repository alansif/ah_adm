<template>
    <div id="app">
        <el-menu theme="dark" mode="horizontal" :router="true">
            <div style="float: right">
            <el-menu-item index="/">处理中心</el-menu-item>
            <el-submenu index="2">
                <template slot="title">我的工作台</template>
                <el-menu-item index="2-1">选项1</el-menu-item>
                <el-menu-item index="2-2">选项2</el-menu-item>
                <el-menu-item index="2-3">选项3</el-menu-item>
            </el-submenu>
            <el-menu-item index="/a">订单管理</el-menu-item>
            </div>
        </el-menu>
        <div class="pagebody">
            <div class="sidebar">
                <el-menu default-active="2" theme="dark">
                    <el-submenu index="1">
                        <template slot="title"><i class="el-icon-message"></i>导航一</template>
                        <el-menu-item-group>
                            <template slot="title">分组一</template>
                            <el-menu-item index="1-1">选项1</el-menu-item>
                            <el-menu-item index="1-2">选项2</el-menu-item>
                        </el-menu-item-group>
                        <el-menu-item-group title="分组2">
                            <el-menu-item index="1-3">选项3</el-menu-item>
                        </el-menu-item-group>
                        <el-submenu index="1-4">
                            <template slot="title">选项4</template>
                            <el-menu-item index="1-4-1">选项1</el-menu-item>
                        </el-submenu>
                    </el-submenu>
                    <el-menu-item index="2"><i class="el-icon-menu"></i>导航二</el-menu-item>
                    <el-menu-item index="3"><i class="el-icon-setting"></i>导航三</el-menu-item>
                </el-menu>
            </div>
            <div class="cntcontainer">
                <transition name="el-fade-in-linear" mode="out-in">
                    <router-view></router-view>
                </transition>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            }
        },
        methods: {
        }
    }
</script>

<style scoped>
    .pagebody{
        position: absolute;
        top:61px;
        left: 0;
        right: 0;
        bottom: 0;
        width: 100%;
    }
    .sidebar{
        width:200px;
        position: fixed;
        top:61px;
        bottom: 0;
        background-color: #293038;
        overflow-x: hidden;
    }
    .cntcontainer{
        position: absolute;
        width: auto;
        top:0;
        bottom: 0;
        right: 0;
        left: 200px;
        overflow-x: hidden;
        overflow-y: scroll;
        background-color: #eaedf1;
    }
    *, *:before, *:after {
        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
    }
</style>
