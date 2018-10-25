<template>
  <div style="width: 1200px">
    <b-card no-body>
      <b-tabs pills card vertical>
        <b-tab title="基础设置">
          <b-form-group >
            <b-img rounded="circle" width="80" height="80" src="../static/img/101.jpg"/>
            <!--<b-form-file v-model="file" plain></b-form-file><br>-->
            <b-button>选择头像</b-button><br>
            <span>昵称</span> <b-input  placeholder="虎牙寞荒"></b-input><br>
            <span>电子邮件</span>  <b-button>点击绑定</b-button><br>
            <span>手机     182****4059  已验证</span>
            <b-form-radio-group v-model="selected" >
              <span>常用编辑器</span>
              <b-form-radio value="first">富文本</b-form-radio>
              <b-form-radio value="second">Markdown</b-form-radio>
              <br>
              <span>语言设置</span>
              <b-form-radio value="first">中文简体</b-form-radio>
              <b-form-radio value="second">中文繁体</b-form-radio>
              <br>
              <span>接收谁的简信</span>
              <b-form-radio value="first">所有人</b-form-radio>
              <b-form-radio value="second">我关注的人、我发过简信的人</b-form-radio>
              <br>
              <span>提醒邮件通知</span>
              <b-form-radio value="first">所有动态</b-form-radio>
              <b-form-radio value="second">每天未读汇总</b-form-radio>
            </b-form-radio-group>
          </b-form-group>
        </b-tab>
        <b-tab title="个人资料">
          全部简信
        </b-tab>
        <b-tab title="微博认证">
          全部投稿请求
        </b-tab>
        <b-tab title="黑名单">
          收到的喜欢和赞
        </b-tab>
        <b-tab title="赞赏设置">
          全部关注
        </b-tab>
        <b-tab title="账号管理">
          赞赏和付费
        </b-tab>
      </b-tabs>
    </b-card>
  </div>
</template>

<script>
    export default {
        name: "Set"
    }
</script>

<style scoped>

</style>
