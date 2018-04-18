<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
	    <swiper-slide v-for="item of swiperList" :key="item.id">
	    	<img class="swiper-img" :src="item.imgUrl" />
	    </swiper-slide>
	    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
  </div>
</template>

<script>
export default {
	name: 'HomeSwiper',
	data () {
		return {
			swiperOption: {
				pagination: '.swiper-pagination',
				loop: true
			},
			swiperList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/piao/fusion/1712/56/7e62e24499ad4702.jpg_890x330_dd59942e.jpg'
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/9e/b9f4b2498b291e02.jpg_890x330_36ccc796.jpg'
			}]
		}
	}
}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
	  background: #fff !important
	.wrapper
	  overflow: hidden
	  width: 100%
	  height: 0
	  padding-bottom: 37.08%
	  background: #eee
	  .swiper-img
	    width: 100%
</style>