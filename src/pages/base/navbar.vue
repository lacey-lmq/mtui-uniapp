<template>
	<view>
		<mt-navbar fixed title="Navbar" emit="true" :config="pagenav" @backClick="backClick"></mt-navbar>
		<view class="comp">
			<ry-title>
				<mt-navbar title="基础用法"></mt-navbar>
			</ry-title>

			<ry-title title="右侧插槽">
				<mt-navbar title="右侧插槽">
					<template slot="right">新增</template>
				</mt-navbar>
			</ry-title>

			<ry-title title="触发自定义方法">
				<mt-navbar title="触发自定义方法" emit="true" @backClick="navbarEvent"></mt-navbar>
			</ry-title>

			<ry-title title="自定义参数">
				<mt-navbar title="自定义参数" :config="navbarConfig"></mt-navbar>
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
				navbarConfig: {
					bg: "#EF6D6D",
					back: false,
				},
			}
		},
		methods: {
			navbarEvent() {
				console.log("触发自定义方法")
			},
		}
	}
</script>
