<template>
	<div class="wrapper">
		<swiper :options="swiperOption" v-if="showSwiper">
			<swiper-slide v-for="item of swiperList" :key = "item.id">
				<img  class="swiper-img" :src="item.imgUrl" />
			</swiper-slide>


			<div class="swiper-pagination"  slot="pagination"></div>
		</swiper>
    </div>
</template>

<script>
	export default{
		name: 'HomeSwiper',
		props:{
			swiperList: Array
		},
		data: function (){
			return{
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true,
					
				}
				
			}
		},
		computed:{
			showSwiper (){
				return this.swiperList.length
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
	  background: #fff
	.wrapper
		overflow: hidden
		width: 100%
		height: 0
		padding-bottom: 26.5%						  
		.swiper-img
			width: 100%
</style>
