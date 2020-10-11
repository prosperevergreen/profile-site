<template>
	<div class="info d-flex p-3 align-items-center" :style="{ background: color }">
		<div>
			<ul>
				<li>
					<strong>Desription:</strong>
					<p>{{ info.description }}</p>
				</li>
				<li>
					<strong>Technology:</strong>
					<p>
					<ul>
						<li v-for="tech in info.techs" :key="tech">{{tech}}</li>
					</ul>
					</p>
				</li>
				<li>
					<strong>Source Code: </strong>
					<a target="_blank" :href="info.githubRepo">{{title}} (Github)</a>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
	export default {
		props: {
			info: Object,
            title: String,
            color: String
		},
	};
</script>

<style>
	a {
        color:aqua;
	}
	.info {
		height: 100%;
		font-size: calc(100% + 0.5vw);
		color: aliceblue;
	}
</style>