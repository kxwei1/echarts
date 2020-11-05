<template>
  <div class="footer">
    <div class="hader">渠道分布</div>
    <div id="channel-left-footer"></div>
  </div>
</template>

<script>
import echarts from "echarts";

export default {
  components: {},
  props: {},
  data() {
    return {};
  },
  mounted() {
    var myChart = echarts.init(document.getElementById("channel-left-footer"));
    var option = {
      grid: {
        top: "10%",
        left: "10%",
        bottom: "10%",
        containLabel: true,
      },
      // 不显示x轴的相关信息
      xAxis: {
        show: false,
      },
      yAxis: [
        {
          type: "category",
          inverse: true,
          data: ["HTML5", "CSS3", "javascript", "客户厕用电需求配合", "NODE"],
          // 不显示y轴的线
          axisLine: {
            show: false,
          },
          // 不显示刻度
          axisTick: {
            show: false,
          },
          // 把刻度标签里面的文字颜色设置为白色
          axisLabel: {
            color: "#fff",
            fontWeight: "900",
            fontSize: "20",
          },
        },
        {
          data: [702, 350, 610, 793, 664],
          inverse: true,
          // 不显示y轴的线
          axisLine: {
            show: false,
          },
          // 不显示刻度
          axisTick: {
            show: false,
          },
          // 把刻度标签里面的文字颜色设置为白色
          axisLabel: {
            color: "#fff",
          },
        },
      ],
      series: [
        {
          name: "条",
          type: "bar",
          data: [70, 34, 60, 78, 69],
          yAxisIndex: 0,
          zlevel: 1,
          // 修改第一组柱子的圆角
          itemStyle: {
            barBorderRadius: 20,
            // 此时的color 可以修改柱子的颜色
            color: "#7193ff",
          },
          // 柱子之间的距离
          barCategoryGap: 50,
          //柱子的宽度
          barWidth: 10,
          // 显示柱子内的文字
          label: {
            show: false,
          },
        },
        {
          name: "框",
          type: "bar",
          barCategoryGap: 50,
          barWidth: 15,
          yAxisIndex: 1,
          zlevel: 0,
          data: [100, 100, 100, 100, 100],
          itemStyle: {
            color: "#01336a",
            barBorderRadius: 15,
          },
        },
      ],
    };
    myChart.setOption(option);
  },
  methods: {},
  computed: {},
  watch: {},
};
</script>

<style scoped>
.footer,
.footer #channel-left-footer {
  width: 910px;
  height: 375px;
}
.footer .hader {
  margin-top: 30px;
  margin-left: 42px;
  padding-left: 16px;
  font-size: 30px;
  color: #5cdbe5;
  font-weight: 900;
  line-height: 36px;
}
.footer .hader::before {
  position: absolute;
  left: 0;
  width: 1;
  margin-top: 2px;
  margin-left: 50px;
  height: 30px;
  border: 2px solid #02a5ea;
  content: "";
}
</style>
