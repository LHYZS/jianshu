<template>
  <div>
    <b-row>
    <b-col cols="4" v-for="topic in topicList" :key="topic.id">
      <b-navbar>
        <router-link :to="'/c/'+topic.id">
        <img :src="topic.url">
          {{topic.courseName}}
        </router-link>
      </b-navbar>
    </b-col>
      <router-link to="/collections">
        <span class="more">更多热门专题></span>
      </router-link>
    </b-row>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        topicList :[
          {
            "id": 1,
            "url": "https://upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
            "courseName": "@IT·互联网"
          },
          {
            "id": 2,
            "url": "https://upload.jianshu.io/collections/images/76/12.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
            "courseName": "自然科普"
          },
          {
            "id": 3,
            "url": "https://upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
            "courseName": "读书"
          },
          {
            "id": 4,
            "url": "https://upload.jianshu.io/collections/images/21/20120316041115481.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
            "courseName": "简书电影"
          },
          {
            "id": 5,
            "url": "https://upload.jianshu.io/collections/images/21/20120316041115481.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
            "courseName": "故事"
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
