<template>
  <div>
    <h4>专题{{id}}详情</h4>
    <b-row>
      <b-col cols="8">
        <b-media vertical-align="center" class="article-box">
          <img :src="topic.topicUrl" class="article-thumbnail"/>
          <h6 class="mt-0 mb-1 title">{{topic.topicName}}</h6>
          <p class="abstract">
            <span>收藏了{{topic.articleCount}}篇文章,{{topic.fans}}关注</span>
          </p>
        </b-media>
         <b-media right-align vertical-align="center" v-for="item in topic.articleList" :key="item.id">
           <img :src="item.url" slot="aside" style="width: 125px;height: 100px">
           <router-link :to="'/w/'+item.id">
           <h3>{{item.title}}</h3>
           </router-link>
           {{item.summary}}
           <br>
           {{item.nickname}}
           <font-awesome-icon icon="comment-alt" />
           {{item.comments}}
           <font-awesome-icon icon="heart" />
           {{item.likes}}
         </b-media>
      </b-col>
      <!--左面界面-->
      <b-col>
        <span>关注的人</span>
        <div v-for="thing in topic.fansList" :key="thing.authorId">
          <router-link :to="'/p/'+thing.authorId">
          <b-img :src="thing.avatar" rounded="circle" style="width: 48px;height: 48px"></b-img>
          </router-link>
        </div>
      </b-col>
    </b-row>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        id: this.$route.params.id,
        topic: {},
        articleList: [],
        fansList:[]
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        var t = {
          "id": 1,
          "topicName": "读书",
          "topicUrl": "https://upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
          "articleCount": 49535,
          "fans": 1601,
          "description":"fdfdf",
          "creator":"简书",
          "articleList":[
            {
              "id":1,
              "title":"春夏秋冬的你",
              "summary":"遇到阮小姐那年，我还未满十八，那时候我当然不是情窦初开，但也只初识风月浅尝辄止。就像偷吃了路边青红参半的苹果，味涩也微甜。 ...",
              "url":"https://upload.jianshu.io/collections/images/95/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/240/h/240",
              "authorId":1,
              "nickname":"夏小刀就是我",
              "comments":1234,
              "likes":12
            },
            {
              "id":2,
              "title":"她的赌徒爸爸，回家了！",
              "summary":"依依的爸爸大民是一个什么样的人呢？在依依十几岁的时候，爸爸在她眼中是那个可以背着她走几十里路去看病依然不会累的人，是那个可以骑车载...",
              "url":"https://upload-images.jianshu.io/upload_images/14513570-52e92a3e26a3b9f9.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":2,
              "nickname":"家不唐",
              "comments":1234,
              "likes":12
            },
            {
              "id":3,
              "title":"2018-10-18 徘徊在崩溃的边缘：记30岁壮小伙遭遇的一连串医疗误诊",
              "summary":"人在生病时往往最无助，也最脆弱，被病痛折磨的无力感是一种可怕的体验。医院本是病患在绝望中渴求抓住的救命稻草，闻到浓浓的消毒水味，见到慈祥的白大褂...",
              "url":"https://upload-images.jianshu.io/upload_images/7907880-4399bbd5dbb114f0.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
              "authorId":3,
              "nickname":"瑟吉尔",
              "comments":1234,
              "likes":12
            },
          ],
          "fansList":[
            {
              "authorId":1,
              "avatar":"https://upload.jianshu.io/users/upload_avatars/14516759/7aa5cea7-fb60-4024-b739-f31aeae431cf?imageMogr2/auto-orient/strip|imageView2/1/w/32/h/32/format/webp"
            },
            {
              "authorId":2,
              "avatar":"https://upload.jianshu.io/users/upload_avatars/14516848/f2d8c49a-6b40-4a1a-98dc-c8819010905c?imageMogr2/auto-orient/strip|imageView2/1/w/32/h/32/format/webp"
            },
            {
              "authorId":3,
              "avatar":"https://upload.jianshu.io/users/upload_avatars/4835201/e3c04d72-eb85-4bfc-a14d-5ec9b7e937de?imageMogr2/auto-orient/strip|imageView2/1/w/32/h/32/format/webp"
            }
          ]
        };
        this.topic = t;
      } else {
        this.topic = {};
      }
    },
    computed: function () {
      return this.topic;
    }
  }
</script>

<style scoped>

</style>
