<template>
	<div id="app">
		<!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
     -->
		<nav class="navbar navbar-expand-lg navbar-light bg-light sticky-top mb-5">
			<a class="navbar-brand" href="/">𝓜𝔂 𝓓𝓮𝓿 𝔀𝓸𝓻𝓵𝓭</a>
			<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>
			<div class="collapse navbar-collapse justify-content-between" id="navbarNav">
				<ul class="navbar-nav">
					<li class="nav-item">
						<router-link class="nav-link" to="/" exact>Projects</router-link>
					</li>
					<li class="nav-item">
						<router-link class="nav-link" to="/profile">Profile</router-link>
					</li>
				</ul>
				<ul class="navbar-nav">
					<li class="nav-item">
						<a class="nav-link" target="_blank" href="https://github.com/prosperevergreen"><img :src="require('@/assets/GitHub-Mark.png')" alt="github icon"></a>
					</li>
				</ul>
			</div>
		</nav>
		<router-view />
	</div>
</template>

<style>
	.navbar-brand {
		font-size: calc(100% + 0.5vw);
	}
	nav {
		background: rgba(238, 174, 202, 0.8);
		background: radial-gradient(
			circle,
			rgba(238, 174, 202, 0.8) 0%,
			rgba(148, 187, 233, 0.8) 100%
		);
		text-align: center;
	}
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		color: #2c3e50;
	}

	nav .router-link-exact-active {
		color: #007bff !important;
	}
</style>
