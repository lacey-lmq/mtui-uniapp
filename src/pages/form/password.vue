<template>
  <view>
    <mt-navbar fixed title="Password 密码" emit="true" :config="pagenav" @backClick="backClick"></mt-navbar>
    <view class="formPage">
      <ry-title title="自定义配置">
        <view class="formContent">
          <mt-form :formData="passFormData"></mt-form>
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
      passFormData: {
        "field": {
          "password": "",
          "password1": "123",
          "password2": "",
          "password3": "",
          "password4": "",
          "password5": ""
        },
        "property": [
          {
            "type": "password",
            "validate": true,
            "value": "password",
            "text": "密码",
            "placeholder": "请输入密码"
          },
          {
            "type": "password",
            "validate": true,
            "disabled": true,
            "value": "password1",
            "text": "密码",
            "valueShow": "123"
          },
          {
            "type": "password",
            "validate": true,
            "detailshow": true,
            "value": "password2",
            "text": "密码",
            "valueShow": "123"
          },
          {
            "type": "password",
            "validate": true,
            "only": true,
            "value": "password3",
            "text": "密码",
            "icon": "https://ts1.cn.mm.bing.net/th?id=OIP-C.4t6CKFcRe9zK8Kgw2uIAWwHaHa&w=250&h=250&c=8&rs=1&qlt=90&o=6&pid=3.1&rm=2",
            "placeholder": "必填项，不显示星号",
            "valueShow": ""
          },
          {
            "type": "password",
            "validate": true,
            "styleType": "col",
            "value": "password4",
            "text": "密码",
            "placeholder": "输入框占整行",
            "valueShow": ""
          },
          {
            "type": "password",
            "hide": true,
            "value": "password5",
            "text": "密码",
            "placeholder": "不在表单中显示本项"
          }
        ]
      }
    }
  }
}
</script>
