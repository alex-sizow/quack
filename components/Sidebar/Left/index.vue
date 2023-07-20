<script setup>
import {
	ArrowDownCircleIcon,
	BellIcon,
	BookmarkIcon,
	DocumentTextIcon,
	HashtagIcon,
	HomeIcon,
	InboxIcon,
	UserIcon,
} from '@heroicons/vue/24/solid';
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
		<div class="mt-2 space-y-3">
			<div class="mt-2 space-y-3">
				<SidebarLeftTab
					><template v-slot:icon><HomeIcon /></template
					><template v-slot:name>Home</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon><HashtagIcon /></template
					><template v-slot:name>Explore</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon><BellIcon /></template
					><template v-slot:name>Home</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon><InboxIcon /></template
					><template v-slot:name>Messanges</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon><BookmarkIcon /></template
					><template v-slot:name>Bookmarks</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon
						><DocumentTextIcon /></template
					><template v-slot:name>Lists</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon><UserIcon /></template
					><template v-slot:name>Profile</template>
				</SidebarLeftTab>
				<SidebarLeftTab
					><template v-slot:icon
						><ArrowDownCircleIcon /></template
					><template v-slot:name>More</template>
				</SidebarLeftTab>
			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped></style>
