<template>
  <div class="index">
    <Layout>
        <Header>
          <video-header></video-header>
        </Header>
        <Content>
          <Carousel autoplay v-model="bannerList">
            <CarouselItem v-for="item in bannerList" :key="index">
                <div class="demo-carousel">
                  <img class="banner" :src="item.url" alt="">
                </div>
            </CarouselItem>
          </Carousel>
          <Menu mode="horizontal" :theme="theme1" active-name="1">
            <MenuItem name="1">
                <Icon type="ios-paper" />
                首页
            </MenuItem>
            <MenuItem name="2">
                <Icon type="ios-paper" />
                智力早起发
            </MenuItem>
            <MenuItem name="2">
                <Icon type="ios-paper" />
                安全早预防
            </MenuItem>
            <MenuItem name="4">
                <Icon type="ios-paper" />
                兴趣早发现
            </MenuItem>
            <MenuItem name="5">
                <Icon type="ios-paper" />
                礼仪文化
            </MenuItem>
            <MenuItem name="6">
                <Icon type="ios-paper" />
                家长小帮手
            </MenuItem>
          </Menu>
          <div class="first">
            <div class="firstTop">
              <div class="topLeft">今日推荐</div>
              <div class="topRight">精彩不容错过</div>
            </div>
            <div class="intro">
              <div v-for="item in beatifulList" class="beatiful">
                <div class="videoImg">
                  <img class="imgUrl" :src="item.imgurl" alt="">
                </div>
                <div class="videoName">
                  {{item.videoname}}
                </div>
                <div class="videoIntro">
                  {{item.videoIntro}}
                </div>
              </div>
            </div>
          </div>
        </Content>
        <Footer>Footer</Footer>
    </Layout>
  </div>
</template>

<script>
import videoHeader from '../public/header'
export default {
  name: 'index',
  data () {
    return {
      bannerList:[{url:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584704683890&di=bbceb211e8fe6246a1e04524802f9fa4&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201706%2F23%2F20170623192818_JSWxy.jpeg'}]
    }
  },
  components: {
    videoHeader
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.banner{
  width: 100%;
  height: 500px;
}
.firstTop {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 12px;
}
.topLeft {
  font-size:26px;
  color: #333;
  margin-left: 12px;
}
.topRight {
  font-size: 16px;
  color: #666;
  margin-left: 12px;
}
</style>
