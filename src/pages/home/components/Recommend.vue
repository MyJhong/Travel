<template>
	<div>
		<div class="title">热销推荐</div>
		<ul>
			<li class="item border-bottom" v-for="item of recommendList" :key="item.id">

				<img class="item-img" :src="item.imgUrl"/>

				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default{
		name: 'HomeRecommend',
		data () {
			return {
				recommendList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/7a/7ac34ad6cc6e7497a3.img.jpg_200x200_939e55b1.jpg',
					title: '东莞龙凤山庄影视渡假村',
					desc: '与明星的邂逅'
				},{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
					title: '隐贤山庄',
					desc: '与明星的邂逅'
				},{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/84/00648f910d93824808f2781486ca5cb8.water.jpg_200x200_9c0de28d.jpg',
					title: '水立方游泳馆',
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
	.item
		overflow: hidden
		display: flex
		height: 1.9rem
	.border-bottom
		border-bottom: .01rem solid #eee
		.item-img
			width: 1.7rem
			height: 1.7rem
			padding: .1rem			
		.item-info
			flex: 1
			padding: .1rem
			min-width: 0
			.item-title
				line-height: .54rem
				font-size: .32rem
				ellipsis()
			.item-desc
				line-height: .54rem
				color: #ccc
				ellipsis()
			.item-button
				line-height: .44rem
				margin-top: .16rem
				background: #ff9300
				padding: 0 .2rem
				border-radius: 0.6rem
				color: #fff
				ellipsis()
		
</style>
