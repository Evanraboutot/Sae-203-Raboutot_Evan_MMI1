<script setup>

	//Définition de la carte des artistes
	
	const props = defineProps({
		profile: {
			type:Object
		},
		useSosmed: {
			type: Boolean,
			default: true
		}
	})
	
</script>

<template>
	<main class="md:w-4/12 p-6 rounded-xl shadow-lg border-4 border-gray-200 bg-gradient-to-r from-sky-600 to-indigo-700 text-gray-50 mb-6">
		<img :src="profile.avatar" class="rounded-xl mx-auto mb-5" width="200" />
		<div class="text-center">
			<h1 class="text-xl font-semibold">{{ profile.name }}</h1>
			<h3 class="md:text-sm">{{ profile.desc }}</h3>
		</div>

		<slot name="footer"></slot>
		
	</main>
</template>