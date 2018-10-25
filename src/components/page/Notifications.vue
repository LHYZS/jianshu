<template>
  <div style="width: 1200px">
      <b-card no-body>
        <b-tabs pills card vertical>
          <b-tab title="评论">
            收到的评论
          </b-tab>
          <b-tab title="简信">
            全部简信
          </b-tab>
          <b-tab title="投稿请求">
            全部投稿请求
          </b-tab>
          <b-tab title="喜欢和赞">
            收到的喜欢和赞
          </b-tab>
          <b-tab title="关注">
            全部关注
          </b-tab>
          <b-tab title="赞赏和付费">
            赞赏和付费
          </b-tab>
          <b-tab title="其他提醒">
            其他提醒
          </b-tab>
        </b-tabs>
      </b-card>
  </div>
</template>

<script>
    export default {
        name: "Notifications"
    }
</script>

<style scoped>

</style>
