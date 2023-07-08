<script setup>
import { HomeIcon } from '@heroicons/vue/24/solid';
const { defaultTransition } = useTailwindConfig();
</script>

<template>
	<div class="flex flex-col h-screen">
		<div
			class="p-2 my-2 rounded-full hover:bg-red-200 w-min"
			:class="defaultTransition">
			<Nuxt-Link to="/"
				><div class="w-8 h-8"><logo-twitter /></div
			></Nuxt-Link>
		</div>
		<HomeIcon />
	</div>
</template>

<style lang="scss" scoped></style>
