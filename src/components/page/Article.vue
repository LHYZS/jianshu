<template>
   <div>
     <b-media>
       <span style="font-size: 40px">
         {{topic.title}}
       </span>
       <br>
       <b-img :src="topic.avatar" rounded="circle" style="width: 60px;height: 60px"/>
       {{topic.name}}<br>
       <span style="font-size: 20px">
         {{topic.content}}
       </span>
     </b-media><br>
     <span style="font-size: 20px">所有评论</span>
     <b-list-group v-for="item in topic.discussList" :key="item">
       <b-list-group-item>
         {{item.readerName}}<br>
         {{item.readerDiscuss}}
       </b-list-group-item>
     </b-list-group>

   </div>
</template>

<script>
  export default {
    data() {
      return {
        id: this.$route.params.id,
        topic: {},
        discussList:[]
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        var t = {
          "id": 1,
          "title":"别了，简述",
          "avatar":"https://upload.jianshu.io/users/upload_avatars/3343569/3cd46650-54bc-4383-989f-80aacb0c42fe.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
          "name":"江上听雨",
          "content":"七月二十一日注册，到今天，正好来简书两个月。\n" +
            "喜欢写字。至今，捉笔写字整整十年。十年间，收获很多。\n" +
            "但一直苦于找不到一个好的平台安放文字。网易，新浪，豆瓣，美篇，格图，简书，都有过注册。但网易宣布即将解散消息后，内心始终有担心。\n" +
            "美篇，格图过于小众，恐难以长久。新浪，豆瓣现在也让人担心。简书，经营上颇多瑕疵，水平也差强人意，长远看，前景必定不会太好。\n" +
            "在一个地方写字安家，于我来讲，原因无非两条。一是和友人在文字上互相激励。二是有温暖的人在左右。两条若都不能满足，我选择孤独。\n" +
            "于是渐生退意。与其一个人在人群里孤独地热闹，不如在静谧处独自孤独。\n" +
            "眠松卧月枕潮头，风动云生看孤舟。\n" +
            "及此，雨决定退出简书。一边调养身体，一边整理归置旧文字。\n" +
            "幽罗，抱歉雨先失信，不能把给你的情书继续下去！飞扬，抱歉不能继续陪你。你从网易到简书一直读雨的字，雨记在心里。祝福飞扬来日日日是好日！茶香姐最近不上简书，不能告别。雨依然祝福茶香姐安好！\n" +
            "祝福在简书遇到的所有网易人——别了——",
          "discussList":[
            {
              "readerId":1,
              "readerName":"恩菲",
              "readerDiscuss":"很好，非常好。"
            },
            {
              "readerId":1,
              "readerName":"零九二",
              "readerDiscuss":"真棒。"
            },
            {
              "readerId":1,
              "readerName":"冷风了",
              "readerDiscuss":"让人受益匪浅。"
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
