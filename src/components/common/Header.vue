<template>
  <b-navbar toggleable="md" type="light" variant="default" fixed class="box">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <router-link to="/">
      <b-navbar-brand>
        <b-img style="height: 50px; width: 85px" src="../static/img/102.png"/>
      </b-navbar-brand>
    </router-link>

    <b-collapse is-nav id="nav_collapse">
      <b-navbar-nav>

        <b-nav-item v-if="token!=null">
          <router-link to="/">发现</router-link>
        </b-nav-item>


        <b-nav-item v-if="token!=null">
          <router-link to="/subscriptions">关注</router-link>
        </b-nav-item>

        <b-nav-item v-if="token!=null">
          <router-link to="/notifications">消息</router-link>
        </b-nav-item>

        <b-nav-item v-if="token===null">
          <router-link to="/index">首页</router-link>
        </b-nav-item>

        <b-nav-item v-if="token===null">
          <router-link to="/download">下载APP</router-link>
        </b-nav-item>

        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search"/>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#">Aa</b-nav-item>
        <b-nav-item v-if="token===null">
          <router-link to="/sign-in">登陆</router-link>
        </b-nav-item>

        <b-nav-item v-if="token===null">
          <router-link to="/sign-up">注册</router-link>
        </b-nav-item>
        <b-nav-item-dropdown right v-if="token!=null">
          <!-- Using button-content slot -->
          <b-dropdown-item>
            <router-link to="/user">
              个人中心
            </router-link>
          </b-dropdown-item>
          <template slot="button-content">
            <b-img rounded="circle" width="35" height="35" src="../static/img/101.jpg"/>

          </template>
          <b-dropdown-item>
            <router-link to="/set">
              设置
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item href="#">退出</b-dropdown-item>
        </b-nav-item-dropdown>
        <a class="btn write-btn" href="/write">
          写文章
        </a>
      </b-navbar-nav>

    </b-collapse>
  </b-navbar>
</template>
<script>
  import 'bootstrap/dist/css/bootstrap.css'
  import 'jquery/dist/jquery.min'
  import 'bootstrap/dist/js/bootstrap.min'

  export default {
    data() {
      return {
        token: null
      }
    },
    computed: {
      username() {
        let username = localStorage.getItem('ms_username');
        return username ? username : this.name;
      }
    },
    methods: {
      // 用户名下拉菜单选择事件
      handleCommand(command) {
        if (command == 'loginout') {
          localStorage.removeItem('ms_username')
          this.$router.push('/login');
        }
      }

    }
  }
</script>
<style scoped>
  .box {
    border-bottom: 1px solid #eef1f6;
    height: 55px;
  }

  a {
    color: #324157;
  }

  .btn {

  }

  .write-btn {
    float: right;
    width: 100px;
    height: 40px;
    line-height: 24px;
    margin: 8px 15px 0;
    border-radius: 20px;
    font-size: 15px;
    color: #fff;
    background-color: #ea6f5a;
  }
</style>
