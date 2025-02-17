<script setup>
	import { defineProps } from "vue";

	defineProps({
		item: Object,
	});
</script>

<template>
	<div
		class="item"
		:style="{ 'background-image': 'url(' + item.image.url + ')' }">
		<h3>{{ item.title }}</h3>
		<p>{{ item.price }}</p>
	</div>
</template>

<style scoped lang="scss">
	.item {
		aspect-ratio: 0.8;
		width: 100%;
		height: 100%;
		padding: 18px;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		background-size: cover;
		background-position: center;
		background-repeat: no-repeat;
		cursor: pointer;

		&:hover {
			h3 {
				padding-left: 10px;
			}
		}
		@media (max-width: $break-sm) {
			aspect-ratio: 0.8;
		}
		h3 {
			word-break: break-word;
			transition: all 0.3s ease;
		}
		p {
			font-size: 0.6em;
		}
	}
</style>
