<template>
<div id="app" class="wrapper">

  <!-- Main Header -->
  <header class="main-header">
    <!-- Header Navbar -->
    <nav class="navbar navbar-static-top" role="navigation">
      <a href="#" class="logo">
        中心生物样本库
      </a>
      <!-- Navbar Right Menu -->
      <div class="navbar-custom-menu">
        <ul class="nav navbar-nav">
          <li class="dropdown user user-menu my-user">
            <a href="#" class="dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
              <img src="./assets/libs/adminlte/img/user2-160x160.jpg" height="160" width="160" class="user-image" alt="User Image">
              <span class="hidden-xs">管理员</span>
            </a>
            <ul class="dropdown-menu my-dropdown-menu">
              <!-- User image -->
              <li class="user-header">
                <img src="./assets/libs/adminlte/img/user2-160x160.jpg" height="160" width="160" class="img-circle" alt="User Image">
                <p>
                  管理员
                  <small>嘉和美康测试医院</small>
                </p>
              </li>
              <!-- Menu Footer-->
              <li class="user-footer">
                <div class="pull-left">
                  <a href="#" class="btn btn-default btn-flat">注销</a>
                </div>
                <div class="pull-right">
                  <a href="#" class="btn btn-default btn-flat">退出</a>
                </div>
              </li>
            </ul>
          </li>
          <!-- Messages: style can be found in dropdown.less-->
          <li class="messages-menu" v-for="menu in menus">
            <!-- Menu toggle button -->
            <a class="" :href="menu.url">
              {{menu.text}}
            </a>
          </li>
          <!-- /.messages-menu -->
          <li class="dropdown">
                <a href="#" class="dropdown-toggle my-dropdown-menu" data-toggle="dropdown">系统菜单<span class="caret"></span></a>
                <ul class="dropdown-menu" role="menu">
                  <li v-for="menu in sysmenu"><a :href="menu.url">{{menu.text}}</a></li>
                </ul>
              </li>
        </ul>
      </div>
    </nav>
  </header>
  


  <!-- Content Wrapper. Contains page content -->
  <div class="content-wrapper">
    <router-view></router-view>
  </div>
    
  <!-- /.content-wrapper -->

  <!-- Main Footer -->
  <footer class="main-footer my-footer">
    <!-- To the right -->
    <div class="pull-right hidden-xs">
      
    </div>
    <!-- Default to the left -->
    <strong>Copyright &copy; 2016 <a href="#">北京嘉和美康信息技术有限公司</a>.</strong> All rights reserved.
  </footer>
</div>

</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      menus: [
        {
          text: '首页',
          url: '#index'
        },
        {
          text: '修改密码',
          url: '#'
        },
        {
          text: '记事本',
          url: '#'
        }
      ],
      sysmenu: [
        {
          text: '平台配置',
          url: '#platform'
        },
        {
          text: '入库管理',
          url: '#in'
        },
        {
          text: '项目配置',
          url: '/ss'
        }
      ]
    }
  },
  created() {

  },
  mounted() {

  }
}
</script>

<style>
.my-footer{
  position: fixed;
  bottom: 0;
  width: 100%;
}
.my-user{
  position: relative !important;
}
.my-dropdown-menu{
  right: 0 !important;
}
.skin-blue .main-header .logo{
  background-color: transparent;
  text-align: left;
}
</style>
