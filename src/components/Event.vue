<template>
	<main>
		<h1 class="text-center pb-6 text-3xl md:text-4xl lg:text-5xl font-semibold text-indigo-500">Artistes</h1>
		<p class="text-gray-600 text-center lg:px-24">Voici les différents artistes qui seront présents sur scène:</p>
		<section class="mt-12 md:flex justify-evenly gap-6">
			<template v-for="(contact, x) in contacts" :key="x">
				<CardProfile :useSosmed="false" :profile="contact">
					<template v-slot:footer>
					</template>
				</CardProfile>
			</template>
		</section>
	</main>
</template>

<script setup>
	import contacts from '@/contacts.js'
	import CardProfile from '@/components/CardProfile.vue'
</script>
