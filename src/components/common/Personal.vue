<template>
  <div>
    <b-row>
      <b-col cols="6" v-for="(item,index) in courses" :key="index">
        <b-navbar>
          <b-img :src="item.url" rounded="circle" style="width: 80px;height: 80px"></b-img>
          {{item.name}}<br>
          {{item.number1}}关注
          {{item.number2}}粉丝
          {{item.number3}}文章
          {{item.number4}}字数
          {{item.number5}}收获喜欢
        </b-navbar>
      </b-col>
    </b-row>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        courses: courses,
      }
    }
  }
  let courses = [
    {
      "id": 1,
      "url": "https://upload.jianshu.io/users/upload_avatars/3627484/eb973bb9-37ba-4d07-acec-850c0a66d1bb.png?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
      "name":"虎牙寞荒",
      "number1":"3",
      "number2":"2",
      "number3":"7",
      "number4":"3305",
      "number5":"0",
    }
  ]
</script>

<style scoped>

</style>
