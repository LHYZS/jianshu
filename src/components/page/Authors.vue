<template>
  <b-row>
    <b-img style="width: 1000px;height: 120px" src="../static/img/author.png"/>
    <b-col cols="4" v-for="topic in topicList" :key="topic.id">
      <div class="collection-wrap">
        <router-link :to="'/c/'+topic.id">
          <b-img :src="topic.topicUrl"  rounded="circle" width="100px" height="100px"/>
          <h5>{{topic.topicName}}</h5>
        </router-link>
        <span>{{topic.summary}}</span>
        <p>
          <b-button variant="success">关注</b-button>
        </p>
        <p>
          <span>最近更新</span><br>
          <span>{{topic.new}}</span>
        </p>
      </div>
    </b-col>
  </b-row>
</template>

<script>
  export default {
    data() {
      return {
        topicList: [
          {
            "id": 1,
            "topicUrl": "https://upload.jianshu.io/users/upload_avatars/5545154/1a3d5ed6-9ad1-44b3-9457-3e6a29dd1b71.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "徐林Grace",
            "summary": "全球营养专家，时尚妈咪特邀",
            "new":"朝圣：经历到天堂和地狱真实存在..."
          },
          {
            "id": 2,
            "topicUrl": "https://upload.jianshu.io/users/upload_avatars/13213889/7314c5cc-ca7f-4542-b914-2c8dffaf324d.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "无限猴子",
            "summary": "一只有限写作的无限猴子",
            "new":"感官少年的咏叹调2.1.3迷幻公园"
          },
          {
            "id": 3,
            "topicUrl": "https://upload.jianshu.io/users/upload_avatars/12665193/828a449f-efbb-4540-b0af-f6c314810515.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "宇文",
            "summary": "既编过学术大作，也做过畅销小说",
            "new":"丝绸之路密码·天山秘径16鸽舍里的人"
          },
          {
            "id": 4,
            "topicUrl": "https://upload.jianshu.io/users/upload_avatars/3730494/4a86a2a7-d5b9-47f1-969a-d8ef4711488b.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "徐林Grace",
            "summary": "全球营养专家，时尚妈咪特邀",
            "new":"朝圣：经历到天堂和地狱真实存在..."
          },
          {
            "id": 5,
            "topicUrl": "https://upload.jianshu.io/users/upload_avatars/5205317/1179d71b-e7c6-4023-89e8-bba25f88272b.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "徐林Grace",
            "summary": "全球营养专家，时尚妈咪特邀",
            "new":"朝圣：经历到天堂和地狱真实存在..."
          },
          {
            "id": 6,
            "topicUrl": "https://upload.jianshu.io/users/upload_avatars/8723996/5b2500d0-9768-4d3e-831c-47526ec444ed.jpeg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "徐林Grace",
            "summary": "全球营养专家，时尚妈咪特邀",
            "new":"朝圣：经历到天堂和地狱真实存在..."
          }
        ]
      }
    }
  }
</script>

<style scoped>

</style>
