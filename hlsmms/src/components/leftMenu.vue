<template>
    <el-aside width="230px">
      <div id="leftTitle">
        <h1>华联超市管理系统</h1>
        <p>你好！ Admin</p>
        <p>
          <router-link to="/">管理首页</router-link> |
          <router-link to="/">退出系统</router-link>
        </p>
      </div>

      <el-menu
        :default-active="$route.path"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
        :unique-opened="true"
      >
        <el-submenu index="1">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>分类管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="/sortmanagement"><router-link to="/sortmanagement">分类管理</router-link></el-menu-item>
            <el-menu-item index="/addcategory"><router-link to="/addcategory">添加分类</router-link></el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>商品管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="/goodsmanagement"><router-link to="/goodsmanagement">商品管理</router-link></el-menu-item>
            <el-menu-item index="/addproduct"><router-link to="/addproduct">添加商品</router-link></el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>进货管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="/stocklist"><router-link to="/stocklist">库存管理</router-link></el-menu-item>
            <el-menu-item index="/addstock"><router-link to="/addstock">添加库存</router-link></el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="4">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>出货管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1">销售列表</el-menu-item>
            <el-menu-item index="1-2">商品出库</el-menu-item>
            <el-menu-item index="1-3">商品退货</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="5">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>统计管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1">销售统计</el-menu-item>
            <el-menu-item index="1-2">进货统计</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="6">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>账号管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="/userlist"><router-link to="/userlist">账号管理</router-link> </el-menu-item>
            <el-menu-item index="/useradd"> <router-link to="/useradd">添加账号</router-link> </el-menu-item>
            <el-menu-item index="/pwdedit"><router-link to="/pwdedit">密码修改</router-link></el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="7">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>会员管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1"> <router-link to="">账号管理</router-link> </el-menu-item>
            <el-menu-item index="1-2"><router-link to="">添加账号</router-link></el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="8">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span>系统管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1">系统信息</el-menu-item>
            <el-menu-item index="1-2">系统配置</el-menu-item>
            <el-menu-item index="1-3">权限管理</el-menu-item>
            <el-menu-item index="1-4">添加管理组</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
      </el-menu>
    </el-aside>
</template>
<script>
export default {
    methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>

</style>
