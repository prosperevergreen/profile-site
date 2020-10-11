<template>
	<div class="project-title row" @click="toggleOpen = !toggleOpen">
		<div class="col">
			<div  :style="{ color: color }">{{title}}</div>
		</div>
		<div class="col-1">
			<svg v-if="toggleOpen" width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-chevron-compact-left" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
				<path fill-rule="evenodd" d="M9.224 1.553a.5.5 0 0 1 .223.67L6.56 8l2.888 5.776a.5.5 0 1 1-.894.448l-3-6a.5.5 0 0 1 0-.448l3-6a.5.5 0 0 1 .67-.223z" />
			</svg>
			<svg v-else width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-chevron-compact-down" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
				<path fill-rule="evenodd" d="M1.553 6.776a.5.5 0 0 1 .67-.223L8 9.44l5.776-2.888a.5.5 0 1 1 .448.894l-6 3a.5.5 0 0 1-.448 0l-6-3a.5.5 0 0 1-.223-.67z" />
			</svg>
		</div>
	</div>
</template>

<script>
	export default {
		props: {
			title: String,
			color: String,
		},
		data: () => ({
			toggleOpen: false,
		}),
	};
</script>

<style scoped>
	.project-title {
		font-family: "Raleway", sans-serif;
		font-size: calc(100% + 3vw);
		font-weight: 800;
		text-align: center;
		border-top: 1px solid gray;
	}
</style>