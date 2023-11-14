<template>
  <dv-full-screen-container>
    <div class="page-content">
      <div class="box-header">
        <dv-border-box-1 class="header">工业互联网标识解析二级节点（鹰潭）</dv-border-box-1>
      </div>
      <div class="boxes-container">
        <div class="box-prefix">
          <dv-scroll-ranking-board :config="enterprise" style="width:100%;height:100%" />
        </div>
        <div class="box-center">
          <div class="map">
            <div class="show1">注册企业103家</div>
            <div class="show2">应用模式数8</div>
            <div class="show3">累计注册量182,962,836</div>
            <div class="show4">累计解析量682,759,844</div>
          </div>
        </div>
        <div class="box-suffix">
          <div class="suffix-top">
            <dv-capsule-chart :config="suffixTop" style="width:100%;height:100%" />
          </div>
          <div class="suffix-bottom">
            <dv-capsule-chart :config="suffixBottom" style="width:100%;height:100%" />
          </div>
        </div>
      </div>
    </div>
  </dv-full-screen-container>
</template>

<script>
export default {
  name: 'DashBoard',
  data () {
    return {
      enterprise: {
        rowNum: 10,
        data: [
          {
            name: '周口',
            value: 55123
          },
          {
            name: '南阳',
            value: 12022
          },
          {
            name: '西峡',
            value: 78932
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '驻马店',
            value: 63411
          },
          {
            name: '新乡',
            value: 44231
          }
        ]
      },
      suffixTop: {
        data: [
          {
            name: '南阳',
            value: 167
          },
          {
            name: '周口',
            value: 67
          },
          {
            name: '漯河',
            value: 123
          },
          {
            name: '郑州',
            value: 55
          },
          {
            name: '西峡',
            value: 98
          }
        ],
        showValue: true,
        unit: '万'
      },
      suffixBottom: {
        data: [
          {
            name: '南阳',
            value: 167
          },
          {
            name: '周口',
            value: 123
          },
          {
            name: '漯河',
            value: 98
          },
          {
            name: '郑州',
            value: 75
          },
          {
            name: '西峡',
            value: 66
          }
        ],
        colors: ['#e062ae', '#fb7293', '#e690d1', '#32c5e9', '#96bfff'],
        unit: '万',
        showValue: true
      }
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.page-content {
  position: relative;
  height: 100%;
  display: flex;
  flex-direction: column; /* 现在使用列布局 */
  justify-content: flex-start; /* 从顶部开始 */
  align-items: center; /* 水平居中 */
}

.boxes-container {
  display: flex;
  flex-direction: row; /* 水平排列 */
  width: 100%; /* 宽度占据全部可用空间 */
  height: calc(100% - 4%); /* 高度减去 box-header 的高度 */
  justify-content: space-between; /* 元素之间的间距平均分布 */
}

.box-header {
  height: 4%;
  width: 40%;
  position: absolute;
  top: 5%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  font-size: 30px;
  color: white;
}

.header{
  background-color: transparent !important;
}

.box-prefix, .box-suffix {
  /* 示例宽度和高度 */
  width: 20%;
  height: 100%;
  position: relative;
}

.box-center {
  width: 60%;
  height: 100%;
  background-image: url("../assets/box_center_bg.png");
  background-size: 100% 100%;
}

.map {
  width: 100%;
  height: 100%;
  background-image: url("../assets/map.png");
  //background-size: 100% 100%;
  background-size: contain;
  position: relative;
  color: white;
}

.suffix-top, .suffix-bottom {
  width: 100%;
  height: 40%;
}

.suffix-bottom{
  top: 10%;
}
</style>
