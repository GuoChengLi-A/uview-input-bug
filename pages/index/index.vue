<template>
  <view>
    <u-input
        v-model="password"
        placeholder="请输入密码"
        font-size="34rpx"
        color="#2a3030"
        :password="inputType"
        border="bottom"
    >
      <template slot="suffix">
        <view class="icon-slots" @click="switchInputType">
          <u-image v-show="!inputType"
                   width="40rpx"
                   height="40rpx"
                   src="@/static/in-icon_display.png" alt=""/>

          <u-image v-show="inputType"
                   width="40rpx"
                   height="40rpx"
                   src="@/static/in-icon_hide.png" alt=""/>
        </view>
      </template>
    </u-input>
  </view>
</template>

<script>
export default {
  data() {
    return {
      password: 'Hello',
      inputType: false
    }
  },
  onLoad() {

  },
  methods: {
    switchInputType() {
      this.inputType = !this.inputType
    }
  }
}
</script>

<style lang="scss">
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200 rpx;
  width: 200 rpx;
  margin-top: 200 rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50 rpx;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36 rpx;
  color: #8f8f94;
}
</style>
