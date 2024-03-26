<template>
	<!-- 顶部导航 -->
	<div class="top-nav">
		<el-menu :default-active="$route.path" router mode="horizontal">
			<el-menu-item v-for="(item, i) in tabitem" :key="i" :index="item.path">
				{{ item.name }}
			</el-menu-item>
		</el-menu>
	</div>
</template>

<script>
export default {
	name: "TopNav",
	props: {
		tabitem: {
			type: Array,
			default() {
				return [];
			},
		},
	},
};
</script>

<style lang="less" scoped>
.top-nav {
	display: flex;
	width: 100%;
	justify-content: center;

}
.el-menu {
	border: 0;
	background-color: transparent; /* 设置背景颜色为透明 */

}
.el-menu-item {
	color: #474b55;
	height: 45px;
	line-height: 45px;
	font-size: 16px;
	background-clip: text;

}
.el-menu-item:hover{
	background-clip: text;
	color: #000000;
	font-size: 18px;
}

.el-menu--horizontal > .el-menu-item.is-active {
	border-bottom: 2px solid var(--mycompColor);
	font-size: 18px;
	color: var(--mycompColor) !important
	
}

</style>
