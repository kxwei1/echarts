<template>
  <div id="app">
    <!-- //盒子 -->
    <div class="main-box">
      <!-- //左侧渠道盒子 -->
      <div class="channel">
        <!-- //标题 -->
        <div class="header">
          <h1>全渠道诉求</h1>
        </div>
        <!-- //副标题 -->
        <div class="title">
          <div class="left">
            <ul>
              <li>服务请求量: <span>23547</span></li>
              <li>业务量: <span>23547</span></li>
              <li>转派量: <span>16876</span></li>
            </ul>
          </div>
          <div class="right"></div>
        </div>
        <!-- 下方图标盒子 -->
        <div class="box">
          <!-- 左侧 -->
          <div class="channel-left">
            <ChannelLeftTop />
            <ChannelLeftMid />
            <ChannelLeftFooter />
          </div>
          <!-- 中间盒子 -->
          <div class="channel-center">
            <ChannelCenterTop />
            <ChannelCenterFooter />
          </div>
          <!-- 右侧 -->
          <div class="channel-right">
            <ChannelRightTop />
            <ChannelRightMid />
            <ChannelRightFooter />
          </div>
        </div>
      </div>
      <div class="map"></div>
      <div class="workOrder"></div>
    </div>
  </div>
</template>

<script>
import ChannelLeftTop from "./components/channel/channel-left-top.vue";
import ChannelCenterTop from "./components/channel/channel-center-top.vue";
import ChannelLeftMid from "./components/channel/channel-left-mid.vue";
import ChannelLeftFooter from "./components/channel/channel-left-footer.vue";
import ChannelCenterFooter from "./components/channel/channel-center-footer.vue";
import ChannelRightTop from "./components/channel/channel-right-top.vue";
import ChannelRightMid from "./components/channel/channel-right-mid.vue";
import ChannelRightFooter from "./components/channel/channel-right-footer.vue";

export default {
  name: "App",
  components: {
    ChannelLeftTop,
    ChannelLeftMid,
    ChannelLeftFooter,
    ChannelCenterTop,
    ChannelCenterFooter,
    ChannelRightTop,
    ChannelRightMid,
    ChannelRightFooter,
  },
};
</script>

<style>
</style>
