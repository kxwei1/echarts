<template>
  <div class="Top">
    <div class="hader">话务检测</div>
    <div class="footer">
      <div class="top">
        <ul>
          <li>
            <el-button>话务量: 1314</el-button>
          </li>
          <li>
            <el-button>话务量: 1314</el-button>
          </li>
          <li>
            <el-button>自助语音: 3057</el-button>
          </li>
        </ul>
      </div>
      <el-select
        v-model="value"
        placeholder="春节"
        size="mini"
        class="select_right"
      >
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        >
        </el-option>
      </el-select>
      <div id="channel-center-top"></div>
    </div>
  </div>
</template>

<script>
import echarts from "echarts";

export default {
  components: {},
  props: {},
  data() {
    return {
      options: [
        {
          value: "选项1",
          label: "黄金糕",
        },
        {
          value: "选项2",
          label: "双皮奶",
        },
        {
          value: "选项3",
          label: "蚵仔煎",
        },
        {
          value: "选项4",
          label: "龙须面",
        },
        {
          value: "选项5",
          label: "北京烤鸭",
        },
      ],
      value: "",
    };
  },
  mounted() {
    var myChart = echarts.init(document.getElementById("channel-center-top"));
    var option = {
      tooltip: {
        trigger: "axis",
      },
      legend: {
        itemWidth: 35, //宽
        itemHeight: 15, //高

        itemGap: 70, //图例之间的间距
        top: "2%",
        left: "10%",
        data: ["邮件营销", "联盟广告", "视频广告", "直接访问", "搜索引擎"],
        textStyle: {
          color: "rgba(255,255,255,.5)",
          fontSize: "20",
          fontWeight: "bold",
        },
      },

      grid: {
        left: "3%",
        top: "90",
        right: "3%",
        bottom: "10",
        containLabel: true,
      },
      xAxis: [
        {
          type: "category",
          boundaryGap: false,
          // x轴更换数据
          data: [
            "01",
            "02",
            "03",
            "04",
            "05",
            "06",
            "07",
            "08",
            "09",
            "10",
            "11",
            "12",
            "13",
            "14",
            "15",
            "16",
            "17",
            "18",
            "19",
            "20",
            "21",
            "22",
            "23",
          ],
          // 文本颜色为rgba(255,255,255,.6)  文字大小为 12
          axisLabel: {
            textStyle: {
              color: "rgba(255,255,255,.6)",
              fontSize: 12,
            },
          },
          // x轴线的颜色为   rgba(255,255,255,.2)
          axisLine: {
            lineStyle: {
              color: "rgba(255,255,255,.2)",
            },
          },
        },
      ],
      yAxis: [
        {
          name: "单位：个",
          nameTextStyle: {
            color: "#fff",
            fontSize: "15",
            fontWeight: "bold",
            padding: [0, 0, 34, 0],
          },
          type: "value",
          axisTick: {
            show: false,
          },
          axisLine: {
            lineStyle: {
              color: "rgba(255,255,255,.1)",
            },
          },
          axisLabel: {
            textStyle: {
              color: "rgba(255,255,255,.6)",
              fontSize: 12,
            },
          },
          // 修改分割线的颜色
          splitLine: {
            lineStyle: {
              color: "rgba(255,255,255,.1)",
            },
          },
        },
      ],
      series: [
        {
          name: "邮件营销",
          type: "line",
          smooth: true,
          // 单独修改当前线条的样式
          lineStyle: {
            color: "#f5dd5b",
            width: "2",
          },
          // 填充颜色设置
          areaStyle: {
            color: new echarts.graphic.LinearGradient(
              0,
              0,
              0,
              1,
              [
                {
                  offset: 0,
                  color: "rgba(245, 221, 91, 0.8)", // 渐变色的起始颜色
                },
                {
                  offset: 0.8,
                  color: "rgba(1, 132, 213, 0)", // 渐变线的结束颜色
                },
              ],
              false
            ),
            shadowColor: "rgba(0, 0, 0, 0.1)",
          },
          // 设置拐点
          symbol: "circle",
          // 拐点大小
          symbolSize: 8,
          // 开始不显示拐点， 鼠标经过显示
          showSymbol: false,
          // 设置拐点颜色以及边框
          itemStyle: {
            color: "#f5dd5b",
            borderColor: "rgba(221, 220, 107, .1)",
            borderWidth: 12,
          },
          data: [
            30,
            40,
            30,
            40,
            30,
            40,
            30,
            60,
            20,
            40,
            30,
            40,
            30,
            40,
            30,
            40,
            30,
            60,
            20,
            40,
            30,
            50,
            40,
          ],
        },
        {
          name: "联盟广告",
          type: "line",
          smooth: true,
          lineStyle: {
            normal: {
              color: "#00ffea",
              width: 2,
            },
          },
          areaStyle: {
            normal: {
              color: new echarts.graphic.LinearGradient(
                0,
                0,
                0,
                1,
                [
                  {
                    offset: 0,
                    color: "rgba(0, 255, 234, 0.8)",
                  },
                  {
                    offset: 0.8,
                    color: "rgba(0, 255, 234, 0)",
                  },
                ],
                false
              ),
              shadowColor: "rgba(0, 0, 0, 0.1)",
            },
          },
          // 设置拐点 小圆点
          symbol: "circle",
          // 拐点大小
          symbolSize: 5,
          // 设置拐点颜色以及边框
          itemStyle: {
            color: "#f5dd5b",
            borderColor: "rgba(221, 220, 107, .1)",
            borderWidth: 12,
          },
          // 开始不显示拐点， 鼠标经过显示
          showSymbol: false,
          data: [
            130,
            10,
            20,
            40,
            80,
            20,
            90,
            40,
            20,
            140,
            30,
            40,
            130,
            40,
            70,
            40,
            30,
            120,
            20,
            99,
            50,
            20,
            60,
          ],
        },
        {
          name: "视频广告",
          type: "line",
          smooth: true,
          lineStyle: {
            normal: {
              color: "#ff7200",
              width: 2,
            },
          },
          areaStyle: {
            normal: {
              color: new echarts.graphic.LinearGradient(
                0,
                0,
                0,
                1,
                [
                  {
                    offset: 0,
                    color: "rgba(214, 109, 4, 0.8)",
                  },
                  {
                    offset: 0.8,
                    color: "rgba(214, 109, 4, 0)",
                  },
                ],
                false
              ),
              shadowColor: "rgba(0, 0, 0, 0.1)",
            },
          },
          // 设置拐点 小圆点
          symbol: "circle",
          // 拐点大小
          symbolSize: 5,
          // 设置拐点颜色以及边框
          itemStyle: {
            color: "#02c0bb",
            borderColor: "rgba(221, 220, 107, .1)",
            borderWidth: 12,
          },
          // 开始不显示拐点， 鼠标经过显示
          showSymbol: false,
          data: [
            110,
            20,
            40,
            60,
            210,
            50,
            70,
            100,
            34,
            90,
            50,
            190,
            50,
            20,
            50,
            50,
            60,
            70,
            70,
            90,
            119,
            30,
            60,
          ],
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

<style  scoped>
.Top{
  height: 850px;

}
.Top #channel-center-top {
  width: 910px;
  height: 715px;
}
.Top .hader {
  position: relative;
  margin-top: 30px;
  margin-left: 42px;
  padding-left: 16px;
  font-size: 30px;
  color: #5cdbe5;
  font-weight: 900;
  line-height: 36px;
}
.Top .hader::before {
  position: absolute;
  left: 0;
  width: 1;
  margin-top: 2px;
  /* margin-left: 50px; */
  height: 30px;
  border: 2px solid #02a5ea;
  content: "";
}
.Top .footer {
  position: relative;
}
.Top .footer .top {
  width: 100%;
  margin: 29px 0;
}
.Top .footer .top ul {
  display: flex;
}
.Top .footer .top ul li {
  text-align: center;
  flex: 1;
}
.el-button {
  border-color: #5cdbe5;
  color: #fff;
  font-weight: bold;
  font-size: 20px;
  background: #02234d;
}
.el-button:hover {
  background: #053879;
  color: #fff;
}
.el-select {
  width: 132px;
}
.el-select /deep/ .el-input__inner {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 20px;
  color: #5cdbe5;
  font-weight: bold;
  padding: 0 26px;
  border: 1px solid #5cdbe5;
}
.el-select /deep/.el-input__suffix {
  border-left: 1px solid #5cdbe5;
  background: #5cdbe5;
  right: 0;
  border-radius: 0px 20px 20px 0;
}
.el-select
  /deep/
  .el-input__suffix
  .el-input__suffix-inner
  .el-icon-arrow-up:before {
  color: #001236;
}
.select_right {
  position: absolute;
  right: 0;
  top: 90px;
  z-index: 1;
}
</style>
