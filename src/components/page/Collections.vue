<template>
  <b-row>
    <b-img style="width: 1000px;height: 120px" src="../static/img/hot.png"/>
    <b-col cols="4" v-for="topic in topicList" :key="topic.id">
      <div class="collection-wrap">
        <router-link :to="'/c/'+topic.id">
          <img :src="topic.topicUrl" width="100px" height="100px"/>
          <h5>{{topic.topicName}}</h5>
        </router-link>
        <span>{{topic.summary}}</span>
        <p>
          <b-button variant="success">关注</b-button>
        </p>
        <p>
          <span>{{topic.articleCount}}篇文章</span>
          <span>{{topic.fans}}个关注</span>
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
            "topicUrl": "https://upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "@IT·互联网",
            "summary": "欢迎关注公共号简宝玉",
            "articleCount": "4598",
            "fans": "129.3k"
          },
          {
            "id": 2,
            "topicUrl": "https://upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "摄影",
            "summary": "欢迎关注公共号简宝玉",
            "articleCount": "3233",
            "fans": "323.3k"
          },
          {
            "id": 3,
            "topicUrl": "https://upload.jianshu.io/collections/images/95/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "故事",
            "summary": "欢迎关注公共号简宝玉",
            "articleCount": "2344",
            "fans": "329.3k"
          },
          {
            "id": 4,
            "topicUrl": "https://upload.jianshu.io/collections/images/21/20120316041115481.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "简书电影",
            "summary": "欢迎关注公共号简宝玉",
            "articleCount": "2983",
            "fans": "934.7k"
          },
          {
            "id": 5,
            "topicUrl": "https://upload.jianshu.io/collections/images/13/%E5%95%8A.png?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "旅行·在路上",
            "summary": "欢迎关注公共号简宝玉",
            "articleCount": "1746",
            "fans": "294.5k"
          },
          {
            "id": 6,
            "topicUrl": "https://upload.jianshu.io/collections/images/283250/%E6%BC%AB%E7%94%BB%E4%B8%93%E9%A2%98.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
            "topicName": "手绘",
            "summary": "欢迎关注公共号简宝玉",
            "articleCount": "2365",
            "fans": "145.3k"
          }
        ]
      }
    }
  }
</script>

<style scoped>

</style>
