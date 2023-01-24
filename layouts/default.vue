<template>
	<div class="main-wrapper bg-light">
		<vs-navbar center-collapsed text-white  target-scroll="#padding-scroll-content" color="primary"  v-model="active">
			<template #left>
				<vs-button size="large" href="/">RickNMorty</vs-button>
			</template>
			<vs-navbar-item :active="active == 'home'" id="home" to="home">
				Home
			</vs-navbar-item>
			<vs-navbar-item :active="active == 'characters'" id="characters" to="characters">
				Characters
			</vs-navbar-item>
			<vs-navbar-item :active="active == 'places'" id="places" to="places">
				Places
			</vs-navbar-item>
			<vs-navbar-item :active="active == 'episodes'" id="episodes" to="episodes">
				Episodes
			</vs-navbar-item>
			<template #right>
				<vs-button flat color="light">About</vs-button>
				<!-- <vs-button>Get Started</vs-button> -->
			</template>
		</vs-navbar>
		<div class="container mx-auto " style="padding-top: 5rem; height: 100%; min-height: 85vh" id="padding-scroll-content">
			<nuxt-child />
		</div>
	</div>

</template>

<script>
export default {
	name: 'IndexPage',
	data() {
		return {
			active: 'home'
		}
	}
}
</script>
