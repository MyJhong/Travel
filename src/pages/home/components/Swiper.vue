<template>
	<div class="wrapper">
		<swiper :options="swiperOption" >
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
		data: function (){
			return{
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true
				},
				swiperList: [{
					id: '0001',
					imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/8f7bcfbd2ccdd8aaa116799a39c812c9.jpg_750x200_c41c49fb.jpg'
				},{
					id: '0002',
					imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
				}]
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
		padding-bottom: 28%						  
		.swiper-img
			width: 100%
</style>
