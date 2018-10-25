<template>
  <div>
    <b-row>
      <b-col cols="12" v-for="(item,index) in courses" :key="index">
        <b-navbar>
          <b-img :src="item.url" rounded="circle" style="width: 48px;height: 48px"></b-img>
          {{item.Name}}<br>
          写了{{item.Number1}}k字·{{item.Number2}}k喜欢
          <div>+关注</div>
        </b-navbar>
      </b-col>
      <router-link to="/authors">
      <b-button>查看全部></b-button>
      </router-link>
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
      "Name":"简书大学堂",
      "Number1":"434.5",
      "Number2":"1.7"
    },
    {
      "id": 2,
      "url": "https://upload.jianshu.io/users/upload_avatars/6305091/b1912e7b-20d1-41a6-94f3-5a0d1c81fc5a.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
      "Name":"一半影子的人",
      "Number1":"504.8",
      "Number2":"1.3"
    },
    {
      "id": 3,
      "url": "https://upload.jianshu.io/users/upload_avatars/3343569/3cd46650-54bc-4383-989f-80aacb0c42fe.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
      "Name":"吴晓布",
      "Number1":"219.6",
      "Number2":"8.7"
    },
    {
      "id": 4,
      "url": "https://upload.jianshu.io/users/upload_avatars/9234143/0819f188-bedf-4878-bbc7-bf08c163314e?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
      "Name":"十七岁的安素",
      "Number1":"422.5",
      "Number2":"6.6"
    },
    {
      "id": 5,
      "url": "https://upload.jianshu.io/users/upload_avatars/11557689/ed2ea7f3-9d7d-41fc-a05a-daebb8097b0c.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
      "Name":"须僧",
      "Number1":"498.3",
      "Number2":"42.8"
    }
  ]
</script>

<style scoped>

</style>
