<template>
	<div id="app">
		<Aside :showAside="showAside"></Aside>
		<div class="app__container">
			<Overlay 
				@listenToggle="toggleNav()"
				:showAside="showAside"
				>
			</Overlay>
			<Header @listenToggle="toggleNav()"></Header>
			<Content></Content>
			<Footer></Footer>
		</div>
	</div>
</template>

<script>
import Aside from './components/Aside.vue'
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'
import Overlay from './components/Overlay.vue'

export default {
	data: () => ({
		showAside: false,
	}),
	methods: {
		toggleNav() {
			this.showAside = !this.showAside
		}
	},
	components: {
		Aside,
		Header,
		Content,
		Footer,
		Overlay,
	}
}
</script>

<style>
	@import '../public/aside.css';
	@import '../public/container.css';
	:root {
		--header-height: 58px;
		--aside-width: 235px;
		--footer-min-height: 120px;
		--content-min-height: calc(100vh - var(--header-height) - var(--footer-min-height));
	}
	html {
		scroll-behavior: smooth;
	}
	html, body {
		padding: 0;
		margin: 0;
	}
	#app {
		display: flex;
	}
	.overlay {
		position: fixed;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background:rgba(37, 37, 37, 0.308);
		z-index: 999;
	}
	/* 
		Extra small devices (portrait phones, less than 576px)
		@media (max-width: 575.98px) {  }
		Small devices (landscape phones, less than 768px)
		@media (max-width: 767.98px) {	}
		Medium devices (tablets, less than 992px)
		@media (max-width: 991.98px) {  }
		Large devices (desktops, less than 1200px)
		@media (max-width: 1199.98px) {  }
	*/
</style>
