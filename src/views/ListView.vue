<template>
  <ListViewHeader :obj="obj"/>
  <ListViewImg  :obj="obj"/>
  <ListMucilFen  :obj="obj"/>
  <ListViewMusiclist  :obj="obj"/>
</template>

<script>
  import {getPlayListDetail} from "@/api";
  import ListViewHeader from "@/components/list-view/ListViewHeader";
  import ListMucilFen from "@/components/list-view/ListMucilFen";
  import ListViewImg from "@/components/list-view/ListViewImg";
  import ListViewMusiclist from "@/components/list-view/ListViewMusiclist";
  import ListViewBack from "@/components/list-view/ListViewBack";
  export default {
    name: "ListView",
    components:{
      ListViewBack,
      ListViewMusiclist,
      ListViewImg,
      ListMucilFen,
      ListViewHeader
    },
    data() {
      let pic={url:'this.obj.imgs'};
      return {
        aaa: [],
        obj: {
          imgs: [],
          names: '',
          pingLun: '',
          description: '',
          shareCount: '',
          avatarUrl: '',
          nickname: '',
          tracks: '',
          tracksLength: '',
        },
        conTop:{
          backgroundImage:'url('+pic.url+')'
        },

      }
    },
    created() {
      //  通过id向后端要数据
      this.getPlayListMusic()
    },
        //   要到数据后，更新自己的data
        methods: {
          async getPlayListMusic() {
            //2.使用this.$router.query来接收传来的参数
            //3.根据参数id向后台查找对应的歌单里的歌曲等数据信息
            const res = await getPlayListDetail(this.$route.query.id, this.$route.query.picture)
            console.log(res.data)
            //更新数据后，更新自己的data
            this.obj.imgs = res.data.playlist.coverImgUrl
            this.obj.names = res.data.playlist.name
            this.obj.pingLun = res.data.playlist.commentCount
            this.obj.description = res.data.playlist.description
            this.obj.shareCount = res.data.playlist.shareCount
            this.obj.avatarUrl = res.data.playlist.creator.avatarUrl
            this.obj.nickname = res.data.playlist.creator.nickname
            this.obj.tracks = res.data.playlist.tracks
            this.obj.tracksLength = res.data.playlist.tracks.length
          }
        }
  }
</script>

<style scoped>

</style>