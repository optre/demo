<template>
  <div class="hello">
    <select v-model="sheng" placeholder="请选择省" @change="chooseSheng">
      <option v-for="item in shengData" :key="item.value" :label="item.label" :value="item.value"></option>
    </select>
    <select v-model="shi" placeholder="请选择市" @change="chooseshi">
      <option v-for="item in shiData" :key="item.value" :label="item.label" :value="item.value"></option>
    </select>
  </div>
</template>

<script>
// 引入
import area from "@/assets/area.js"
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      shengData: [], //省data
      shiData: [], //市data
      sheng: '',//省
      shi: ''// 市
    }
  },
  created () {
    // area.forEach(v => {
    //   this.shengData.push({ label: v.label, value: v.value })
    // });
  },
  mounted () {

  },
  methods: {
    chooseSheng (obj) {
      area.forEach(vv => {
        if (vv.value == obj.target.value) {
          // 设置市
          this.shiData = vv.children
        }
      }
      )
    },
    chooseshi () {
      // 获取省市值
      console.log(this.sheng, this.shi)
    }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
