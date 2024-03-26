<template>
	<div id="app" >
		<!-- 头部 -->
		<Header />
		<!-- 主体 -->
		<Main />
		<!-- 底部 -->
		<Footer />
	</div>
</template>
<script>
import Header from "./layout/Header.vue";
import Main from "./layout/Main.vue";
import Footer from "./layout/Footer.vue";
export default {
	name: "App",
	components: { Header, Main, Footer },
};
</script>

<style scoped>
@import "assets/css/base.css";	
#app {
	width: 100%;
	height: 100vh;
	position: fixed;
	
	background-image:url(~assets/imgs/hyrz.png);
	/* background-image:var(--themeImg); */
	background-size: cover;
	background-position: center;
	position: relative;
	z-index: 1;
}
#app::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  backdrop-filter: blur(10px); /* 设置模糊效果的强度 */
  z-index: -1;
  
}

</style>
