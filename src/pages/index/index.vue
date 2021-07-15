<template>
  <view class="content">
    <view class="swiper-wrap">
      <swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="2000" :duration="500">
        <swiper-item>
          <image mode="aspectFit" src="@/static/banner.png"></image>
        </swiper-item>
        <swiper-item>
          <image mode="aspectFit" src="@/static/banner.png"></image>
        </swiper-item>
        <swiper-item>
          <image mode="aspectFit" src="@/static/banner.png"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="info-wrap">
      <view class="info-item">
        <view class="info-item-item">
          <view class="yellow-dian-wrap">
            <view class="yellow-item yellow-item-1"></view>  
            <view class="yellow-item yellow-item-2"></view>  
            <view class="yellow-item yellow-item-3"></view>  
            <view class="yellow-item yellow-item-4"></view>  
          </view>  
          <view class="item-title">商品购买</view>
        </view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <!-- 更多btn -->
        <view class="more-btn">
          <view class="line"></view>
          <view class="line"></view>
          <view class="line"></view>
        </view>
      </view>
      <view class="info-item">
        <view class="info-item-item">
          <view class="yellow-dian-wrap">
            <view class="yellow-item yellow-item-1"></view>  
            <view class="yellow-item yellow-item-2"></view>  
            <view class="yellow-item yellow-item-3"></view>  
            <view class="yellow-item yellow-item-4"></view>  
          </view>  
          <view class="item-title">防疫物资</view>
        </view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <!-- 更多btn -->
        <view class="more-btn">
          <view class="line"></view>
          <view class="line"></view>
          <view class="line"></view>
        </view>
      </view>
      <view class="info-item">
        <view class="info-item-item">
          <view class="yellow-dian-wrap">
            <view class="yellow-item yellow-item-1"></view>  
            <view class="yellow-item yellow-item-2"></view>  
            <view class="yellow-item yellow-item-3"></view>  
            <view class="yellow-item yellow-item-4"></view>  
          </view>  
          <view class="item-title">附近好店</view>
        </view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <view class="info-item-item"></view>
        <!-- 更多btn -->
        <view class="more-btn">
          <view class="line"></view>
          <view class="line"></view>
          <view class="line"></view>
        </view>
      </view>
    </view>
    <view class="map-wrap">
      <map :latitude="latitude" :longitude="longitude" :markers="covers"> </map>
    </view>
    <image class="custom-us" mode="widthFix" src="@/static/custom-us.png"></image>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        latitude: 39.909,
        longitude: 116.39742,
        covers: [
          {
            latitude: 39.909,
            longitude: 116.39742,
            iconPath: '../../static/location.png',
          },
          {
            latitude: 39.9,
            longitude: 116.39,
            iconPath: '../../static/location.png',
          },
        ],
      }
    },
    onLoad() {},
    methods: {},
  }
</script>

<style>
  uni-page-body {
    height: auto;
    min-height: 100%;
    background: url('~@/static/bg.png') no-repeat;
    background-size: cover;
    background-position: center top;
  }
  .content {
    width: 90%;
    margin: 0 auto;
  }
  .swiper {
    width: 100%;
    height: 400rpx;
  }
  .swiper swiper-item {
    border-radius: 20rpx;
  }
  .swiper image {
    width: 100%;
    height: 400rpx;
  }
  ::v-deep .swiper .uni-swiper-dots {
    bottom: 60rpx;
  }
  .info-wrap {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .info-wrap .info-item {
    width: 30%;
    height: 280rpx;
    background: #fefefe;
    border-radius: 30rpx;
    flex-shrink: 0;
    /* overflow: hidden; */
    display: flex;
    flex-direction: column;
    position: relative;
  }
  .info-item .more-btn {
    position: absolute;
    bottom: -10rpx;
    left: 0;
    min-width:  72rpx;
    height: 33rpx;
    background: linear-gradient(to right, #f5c24c 0%,#f4a44c 100%);
    border-radius: 20rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .more-btn .line {
    width: 28rpx;
    height: 2rpx;
    background: rgba(255, 255, 255, .6);
    margin-top: 4rpx;
  }
  .more-btn .line:first-child {
    margin-top: 0;
  }
  .info-item-item {
    width: 100%;
    height: 48rpx;
    border-bottom: 2rpx solid #f0f0f0;
    position: relative;
  }
  .yellow-dian-wrap {
    width: 35rpx;
    height: 16rpx;
    position: absolute;
    left: 16rpx;
    top: 16rpx;
    z-index: 1;
  }
  .yellow-item {
    width: 8rpx;
    height: 8rpx;
    background: #f5a34d;
    border-radius: 50%;
    position: absolute;
  }
  .yellow-item-1 {
    left: 0;
    top: 0;
  }
  .yellow-item-2 {
    left: 20rpx;
    top: 0;
  }
  .yellow-item-3 {
    left: 10rpx;
    bottom: 0;
  }
  .yellow-item-4 {
    bottom: 0;
    right: 0;
  }
  .info-item-item:nth-of-type(2) {
    box-shadow: 0px -7px 10px #f3f1f1;
  }
  .info-item-item:nth-of-type(5) {
    box-shadow: 0px 4px 10px #f3f1f1;
  }
  .info-item-item .item-title {
    color: black;
    font-size: 16rpx;
    font-weight: 500;
    position: absolute;
    left: 40rpx;
    top: 10rpx;
    z-index: 2;
  }
  .map-wrap {
   margin-top: 60rpx;
  }
  .map-wrap map {
    width: 100%;
    height: 400rpx;
  }
  .custom-us {
    position: absolute;
    bottom: 20rpx;
    left: 20rpx;
    width: 280rpx;
  }
</style>
