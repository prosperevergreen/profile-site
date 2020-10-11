<template>
	<div class="home my-5">
		<app-project-section :projectData="data" v-for="(data,i) in projects" :key="i" />
	</div>
</template>

<script>
	// @ is an alias to /src
	import AppProjectSection from "@/components/ProjectSection.vue";

	export default {
		name: "Home",
		components: {
			AppProjectSection,
		},
		data: () => ({
			projects: [
				{
					id: "tictactoe",
					picInfoOrder: true,
					img: "TicTacToe.gif",
					title: "𝕋𝕚𝕔-𝕋𝕒𝕔-𝕋𝕠𝕖 𝔸𝕡𝕡",
					color: "#00573f",
					info: {
						description:
							"This is a game for two players that can strengthening the ability to think strategically and plan ahead.",
						techs: [
							"UIStoryboard",
							"Struct",
							"Auto layout",
							"Dynamically changing UI",
						],
						githubRepo:
							"https://github.com/prosperevergreen/TicTacToe-iOS",
					},
				},
				{
					id: "calculator",
					picInfoOrder: false,
					img: "Calculator.gif",
					title: "ℂ𝕒𝕝𝕔𝕦𝕝𝕒𝕥𝕠𝕣 𝔸𝕡𝕡",
					color: "#35577F",
					info: {
						description:
							"A simple calculator app. Useful for solving basic algebraic problem",
						techs: [
							"UIStoryboard",
							"Struct",
							"Computed Properties",
							"Auto layout",
							"Stack view",
							"Dynamically changing UI",
						],
						githubRepo:
							"https://github.com/prosperevergreen/CalculatorApp-iOS-13",
					},
				},
				{
					id: "todo",
					picInfoOrder: true,
					img: "Todo.gif",
					title: "𝕋𝕠𝔻𝕠 𝔸𝕡𝕡",
					color: "#6D4F2E",
					info: {
						description:
							"A simple ToDo app for managing, checking and deleting your tasks.",
						techs: [
							"Persistence Data",
							"Realm",
							"Core Data",
							"UI Storyboard",
							"UITableView",
							"Dynamically manipulating UI",
							"CocoaPod",
						],
						githubRepo:
							"https://github.com/prosperevergreen/TodoApp-iOS13",
					},
				},
			],
		}),
	};
</script>
