<template>
	<div class="container-fluid">
		<div class="row">
			<div class="col-12">
				<app-title-section :title="projectData.title" :color="projectData.color" data-toggle="collapse" :data-target="`#${projectData.id}`" aria-expanded="true" :aria-controls="projectData.id"/>
			</div>
			<div class="col-12 show" :id="projectData.id">
				<div class="row">
          <!-- order the picture and info based to alternate -->
					<div class="col-md-6 p-0" :class="[projectData.picInfoOrder ? 'order-md-1' : 'order-md-2']">
						<app-pic-section :image="projectData.img" />
					</div>
					<div class="col-md-6 p-0" :class="[!projectData.picInfoOrder ? 'order-md-1' : 'order-md-2']">
						<app-info-section :info="projectData.info" :title="projectData.title" :color="projectData.color"/>
					</div>
				</div>
			</div>

		</div>
	</div>
</template>

<script>
	// @ is an alias to /src
	import AppTitleSection from "@/components/TitleSection.vue";
	import AppPicSection from "@/components/PicSection.vue";
	import AppInfoSection from "@/components/InfoSection.vue";

	export default {
		name: "Home",
		components: {
			AppTitleSection,
			AppPicSection,
			AppInfoSection,
		},
		props: {
      projectData: Object
		},
	};
</script>
