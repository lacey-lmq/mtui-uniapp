<template>
  <view>
    <mt-navbar fixed title="List 列表" emit="true" :config="pagenav" @backClick="backClick"></mt-navbar>
    <view class="formPage">
      <ry-title title="自定义配置">
        <view class="formContent">
          <mt-form :formData="listFormData" @change="changeList"></mt-form>
        </view>
      </ry-title>
    </view>
  </view>
</template>

<script>
import common from "../../common/common.js";

export default {
  mixins: [common],
  data() {
    return {
      listFormData: {
        "field": {
          "list": "第三个哦",
          "list1": "",
          "list1-text": ""
        },
        "property": [
          {
            "type": "list",
            "validate": true,
            "options": [
              {
                "id": 0,
                "value": "第一个哦",
                "brief": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "id": 1,
                "value": "第二个哦",
                "brief": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "id": 2,
                "value": "第三个哦",
                "brief": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "id": 3,
                "value": "第四个哦",
                "brief": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "id": 4,
                "value": "第五个哦",
                "brief": "详情地址详情地址详情地址详情地址详情地址详情地址"
              }
            ],
            "getKey": "value",
            "text": "详情地址",
            "value": "list",
            "placeholder": "请选择详情地址",
            "showValue": {"key": "id", "value": "value", "brief": "brief"},
            "valueShow": "第三个哦"
          },
          {
            "type": "list",
            "styleType": "col",
            "options": [
              {
                "name": 0,
                "content": "第一个哦",
                "desc": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "name": 1,
                "content": "第二个哦",
                "desc": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "name": 2,
                "content": "第三个哦",
                "desc": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "name": 3,
                "content": "第四个哦",
                "desc": "详情地址详情地址详情地址详情地址详情地址详情地址"
              },
              {
                "name": 4,
                "content": "第五个哦",
                "desc": "详情地址详情地址详情地址详情地址详情地址详情地址"
              }
            ],
            "getKey": "key",
            "text": "详情地址",
            "value": "list1",
            "placeholder": "请选择详情地址",
            "secondValue": "list1-text",
            "showValue": {"key": "name", "value": "content", "brief": "desc"}
          }
        ]
      }
    }
  },
  methods: {
    changeList(item) {
      uni.showToast({
        title: "表单提交的结果：" + JSON.stringify(item),
        icon: "none"
      })
    }
  }
}
</script>
