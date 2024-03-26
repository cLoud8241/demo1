<template>
	<div class="personalized" v-if="personalized.length !== 0">
		<div class="hd">
			<el-divider content-position="left"><h2>推荐歌单 ></h2></el-divider>
		</div>
		<div class="bd">
			<SongList :songlist="personalized" />
		</div>
	</div>
</template>

<script>
import SongList from "components/content/songlist/SongList.vue";
export default {
	components: { SongList },
	name: "Personalized",
	props: {
		personalized: {
			type: Array,
			default() {
				return [];
			},
		},
	},
};
</script>

<style lang="less" scoped>
.el-divider__text{
	background-color: transparent;
	
}
.el-divider--horizontal {
    display: block;
    height: 1px;
	background-color: transparent;
    width: 100%;
    margin: 24px 0;
}


</style>
