<template>
  <div>
      <b-row v-for="(item,index) in course3s" :key="index">
        <b-media right-align vertical-align="center">
          <img :src="item.url" slot="aside" style="width: 125px;height: 100px">
          <h3>{{item.title}}</h3>
          {{item.content}}
    </b-media>
      </b-row>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        course3s: course3s,
      }
    }
  }
  let course3s = [
    {
      "id": 1,
      "url": "https://upload-images.jianshu.io/upload_images/12590023-f4da42a82a184845.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
      "title": "干货：写文收入3000到12000，记录我的四个全职小伙伴。",
      "content": "本来，以为这辈子都戒不了书。因为我属于看书，会看疯魔的小恐怖分子.然而，当我成为一只码字狗后。居然，戒掉了这个陋习。两耳不闻窗外事，一心只想码字。"
    },
    {
      "id": 2,
      "url": "https://upload-images.jianshu.io/upload_images/13439838-413f3e9a49e22bd5.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
      "title": "三生三世枕上书续写10",
      "content": "很快，帝后白凤九怀孕的事已被四海八荒皆知，太晨宫也渐渐地热闹起来，很多人送来许多珍贵的药材，和各种补品，想把这些药材和补品送入帝君与帝后的眼中。"
    },
    {
      "id": 3,
      "url": "https://upload-images.jianshu.io/upload_images/1807778-86afdc61dbead7f2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
      "title": "三生三世枕上书[续写](二)",
      "content": " 是夜，凤九趴在榻上，翻着司命送来的话本子，看得津津有味。“小白，明日我们去碧海苍灵可好?”凤九一听，急忙回应道:“好呀好呀，自我醒来，还没去看过呢!”脸上一派欢。"
    },
    {
      "id": 4,
      "url": "https://upload-images.jianshu.io/upload_images/11865775-8a1ccee3bb6cfe54.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
      "title": "老公生死未卜，婆婆让我跟小叔子传宗接代",
      "content": "她放掉浴缸里的水，然后重新放满清水，轻轻跨进去，拿出一个新的剃须刀片，在自己手腕上用力一划，鲜红的血汩汩流出，流过瓷白的手臂，落在清水里，在水里晕散开来，开成一朵绚丽的红花。"
    },
    {
      "id": 5,
      "url": "https://upload-images.jianshu.io/upload_images/13574966-630c3e5e9ca27d40.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
      "title": "放心",
      "content": "老太太看着坐在门口吃荔枝的儿媳夏怜，嘴角不经意地咧了咧。夏怜胸大、屁股大，很轻易给她生了俩男孙。大的10岁，小的6岁。"
    }
  ]
</script>

<style scoped>

</style>
