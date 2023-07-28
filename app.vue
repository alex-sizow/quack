<script setup>
const darkMode = ref(false);
</script>

<template>
	<div :class="{ dark: darkMode }">
		<div class="bg-white dark:bg-dim-900">
			<div class="min-h-full">
				<!--  Left sidebar  -->
				<div
					class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5">
					<div
						class="hidden md:block md:col-span-3 xl:col-span-4">
						<div class="sticky top-0"><SidebarLeft /></div>
					</div>
					<!-- Main content-->
					<main
						class="col-span-12 bg-red-500 md:col-span-8 xl:col-span-6">
						<h1>main</h1>
					</main>
					<!-- Right sidebar -->
					<div
						class="hidden bg-blue-500 md:block xl:col-span-4 md:col-span-3">
						<div class="sticky top-0">
							<h1>Right Sidebar</h1>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
