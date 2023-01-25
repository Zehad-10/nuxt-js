<template>
	<div>
		<nav class="flex items-center justify-between bg-gray-400 px-10 py-5">
			<NuxtLink to="/">Home</NuxtLink>

			<NuxtLink to="/products">Products</NuxtLink>
		</nav>

		<div>
			<slot />
		</div>
	</div>
</template>

<script setup></script>

<style scoped>
.router-link-active {
	@apply bg-black text-white font-bold p-2 rounded-md;
}
</style>
