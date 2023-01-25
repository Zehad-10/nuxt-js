<template>
	<div class="grid grid-cols-3 gap-36 px-10">
		<div v-for="p in products">
			<img class="w-[200px]" :src="p.image" alt="products image" />
			<h3 class="my-3 font-bold text-2xl">{{ p.title }}</h3>
			<p class="mb-3">{{ p.description }}</p>
			<p class="font-bold text-xl">${{ p.price }}</p>
			<NuxtLink
				class="mt-5 bg-orange-400 inline-block px-10 py-3 rounded-md text-white font-semibold cursor-pointer hover:bg-orange-500"
				:to="`/products/${p.id}`"
				>Read More!</NuxtLink
			>
		</div>
	</div>
</template>

<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style lang="scss" scoped></style>
