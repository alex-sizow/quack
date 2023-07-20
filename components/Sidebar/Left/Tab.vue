<script setup>
const { defaultTransition } = useTailwindConfig();

const props = defineProps({
	active: {
		type: Boolean,
		default: false,
	},
});

const textClasses = computed(() =>
	props.active ? 'font-semibold' : 'font-normal',
);
</script>

<template>
	<nuxt-link
		to="#"
		class="flex items-center p-3 rounded-full w-min hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white">
		<div
			class="w-6 h-6 text-dark"
			:class="defaultTransition">
			<slot name="icon"></slot>
		</div>
		<div
			class="hidden ml-3 text-xl md:block"
			:class="textClasses">
			<slot name="name"></slot></div
	></nuxt-link>
</template>
