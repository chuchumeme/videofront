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
          <div></div>
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
</style>
