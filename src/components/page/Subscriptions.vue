<template>
  <div style="width: 1200px">
    <b-card no-body>
      <b-tabs pills card vertical>
          <b-tab col="9" v-for="(item,index) in course4s" :key="index">
          <template slot="title">
            <b-img :src="item.url" rounded="circle" style="width: 40px;height: 40px"></b-img>
            {{item.Name}}
          </template>
          <b-navbar >
          <b-img :src="item.url" rounded="circle" style="width: 80px;height: 80px"></b-img>
          {{item.Name}}<br>
          写了{{item.Number1}}字，获得了{{item.Number2}}个喜欢
          </b-navbar>
          <v-word></v-word>
          </b-tab>
      </b-tabs>
    </b-card>
  </div>
</template>

<script>
  import vWord from '../common/Word';
  export default {
    components: {
      vWord,
    },
    data() {
      return {
        course4s: course4s,
      }
    }
  }
  let course4s = [
    {
      "id": 1,
      "url": "https://upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
      "Name":"简友圈",
      "Number1":"1701",
      "Number2":"0",
      // "Title":"受封建礼教",
      // "Content":"哦忘了方面"
    },
    {
      "id": 2,
      "url": "https://upload.jianshu.io/users/upload_avatars/12569258/ae6aca77-3712-44c2-ad1c-aecebdd9ad76?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120/format/webp",
      "Name":"默写_0c03",
      "Number1":"1701",
      "Number2":"0",
      // "Title":"受封建礼教",
      // "Content":"哦忘了方面"
    },
    {
      "id": 3,
      "url": "https://upload.jianshu.io/users/upload_avatars/13930986/361dcdf3-798a-41c0-a93e-6815a78fff93?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120/format/webp",
      "Name":"微笑吧_5464",
      "Number1":"2700",
      "Number2":"1",
      // "Title":"受封建礼教",
      // "Content":"哦忘了方面"
    },
    {
      "id": 4,
      "url": "https://upload.jianshu.io/users/upload_avatars/3388039/82924622-c185-47a6-94a4-965a99e71a17.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120/format/webp",
      "Name":"陶然然_niit",
      "Number1":"2550",
      "Number2":"6",
      // "Title":"受封建礼教",
      // "Content":"哦忘了方面"
    },
  ]
</script>

<style scoped>

</style>
