<template>

    <el-container>
        <el-aside width="200px" height="100%">
            <el-menu default-active="2" class="el-menu-vertical-demo" text-color="#909399" active-text-color="#409EFF">
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
                <el-menu-item index="4">导航四</el-menu-item>
            </el-menu>
        </el-aside>
        <el-container>
            <el-header class="header">
                header
            </el-header>
            <el-main class="main">
                main
            </el-main>
        </el-container>




    </el-container>

</template>

<script>
    export default {
        // data() {
        //     return activecolor;
        // },
        // method: {
        //     hoveron() {
        //         this.activecolor = 'background-color:#409EFF'
        //     },
        //     hoverleaver() {
        //         this.activecolor = 'background-color:#F2F6FC'
        //     }
        // }
    }
</script>

<style>
    .el-container {
        height: 100%;
    }

    .el-aside {
        background-color: #F2F6FC;
    }

    .el-aside .el-submenu:hover {
        background-color: #409EFF
    }

    .el-menu {
        text-align: left;
        background-color: transparent;
    }

    .header {
        /* background-color: red; */
    }

    .main {
        /* background-color: pink; */
    }

    .footer {
        /* background-color: yellow; */
    }
</style>