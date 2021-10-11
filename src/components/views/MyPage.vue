<template>

    <el-container>
        <el-aside width="200px" height="100%">
            <el-menu default-active="2" class="el-menu-vertical-demo">
                <el-submenu index="1">
                    <template slot="title">
                        <i class="el-icon-menu"></i>
                        <span>导航一</span>
                    </template>
                    <el-menu-item index="1-1">1111</el-menu-item>
                </el-submenu>
                <el-submenu index="2">
                    <template slot="title">
                        <i class="el-icon-s-order"></i>
                        <span>导航二</span>
                    </template>
                    <el-menu-item index="2-1">2222</el-menu-item>
                </el-submenu>
                <el-submenu index="3">
                    <template slot="title">
                        <i class="el-icon-s-promotion"></i>
                        <span>导航三</span>
                    </template>
                    <el-menu-item index="3-1">333</el-menu-item>
                </el-submenu>
                <el-menu-item index="4">
                    <i class="el-icon-s-shop"></i>
                    <span>导航四</span>
                </el-menu-item>
            </el-menu>
        </el-aside>
        <el-container>
            <el-header>
                <el-image style="width: 180px;height: 100px;" :src="url"></el-image>
                <div style="display: flex;flex-direction: row;align-items: center;">
                    <el-avatar src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar>
                    <span>欢迎您！{{usr}}</span>
                </div>
            </el-header>
            <el-main class="main">
                main
            </el-main>
        </el-container>




    </el-container>

</template>

<script>
    export default {
        name: 'MyPage',
        data() {
            return {
                url: require('../../assets/welcome.jpg'),
                usr: ''
            }
        },
        mounted() {
            this.usr = this.$route.params.usr
        }
    }
</script>

<style>
    .el-container {
        height: 100%;
    }

    .el-aside {
        background-color: #fff;
        color: #909399;
    }

    .el-submenu__title i,
    .el-menu-item i {

        color: #303133;
    }

    .el-submenu__title:hover {
        background-color: rgb(217, 236, 255)
    }

    .el-submenu .el-menu-item:hover {
        background-color: rgb(217, 236, 255)
    }


    .el-menu-item:hover {
        background-color: rgb(217, 236, 255)
    }


    .el-menu {
        text-align: left;
        background-color: transparent;
    }

    .el-header {
        width: 100%;
        height: 100px !important;
        border-bottom: 1px solid #eee;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        background-color: rgb(246, 246, 246);

    }

    .main {
        /* background-color: pink; */
    }
</style>