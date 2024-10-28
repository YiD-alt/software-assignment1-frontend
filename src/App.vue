<template>
  <div id="app">
   <el-container>
    <el-header style="background-color: #4c535a">
    <img src="@/assets/logo.png" alt="" style="width:40px; position:relative; top:10px;">
    <span style="font-size:20px; margin-left:15px;color:white">通讯录管理系统</span>
    </el-header>
   </el-container>
    <el-container>
      <el-aside style="overflow: hidden;min-height: 100vh;background-color:#545c64;width:200px">
       <el-menu
            :default-active="$route.path" router
            class="el-menu-vertical-demo"
            @open="handleOpen"
            @close="handleClose"
            background-color="#545c64"
            text-color="#fff"
            active-text-color="#ffd04b">
             <el-menu-item index="/">
                          <i class="el-icon-menu"></i>
                          <span slot="title">系统首页</span>
                        </el-menu-item>
            <el-submenu index="2">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span>信息管理</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="/admin">信息总览</el-menu-item>
                <el-menu-item index="2-2">信息录入</el-menu-item>
                <el-menu-item index="2-3">信息删除</el-menu-item>
                <el-menu-item index="2-4">信息筛查</el-menu-item>
              </el-menu-item-group>


            </el-submenu>


          </el-menu>
      </el-aside>
      <el-main>
      <router-view/>
      </el-main>
    </el-container>
 </div>
 </template>

 <style>
 .el-menu{
   border-right: none !important;
 }
 </style>


