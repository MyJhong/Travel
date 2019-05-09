<template>
	<div>
		<div class="title">周末去哪儿</div>
		<ul>
			<li class="item border-bottom" v-for="item of recommendList" :key="item.id">

				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl"/>
				</div>

				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default{
		name: 'HomeWeekend',
		data () {
			return {
				recommendList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
					title: '东莞龙凤山庄影视渡假村',
					desc: '与明星的邂逅'
				},{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg',
					title: '东莞龙凤山庄影视渡假村',
					desc: '与明星的邂逅'
				},{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4b/d04aa63b1b0ab3.jpg_r_640x214_a3a9c5b6.jpg',
					title: '东莞龙凤山庄影视渡假村',
					desc: '与明星的邂逅'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped="scoped">
	@import '~styles/mixins.styl'
	.title
		margin-top: .2rem
		line-height: .8rem
		background: #eee
		text-indent: .2rem
	.item-img-wrapper
		overflow: hidden
		height: 0
		padding-bottom: 33.9%
	.border-bottom
		border-bottom: .01rem solid #eee
		.item-img
			widht: 100%		
		.item-info			
			padding: .1rem
			.item-title
				line-height: .54rem
				font-size: .32rem
				ellipsis()
			.item-desc
				line-height: .54rem
				color: #ccc
				ellipsis()
			
		
</style>
