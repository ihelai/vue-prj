<script setup>
	import FooterComp from "./components/FooterComp.vue";
</script>

<template>
	<div id="app">
		<router-view />
		<FooterComp />
	</div>
</template>

<style lang="scss">
	@import "@/assets/scss/style.scss";
</style>
