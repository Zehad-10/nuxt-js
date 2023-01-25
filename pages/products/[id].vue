<template>
	<div
		class="w-[300px] mx-auto text-center shadow-lg bg-slate-200 my-10 py-10 px-4"
	>
		<img class="w-[200px] mx-auto" :src="products.image" alt="products image" />
		<h3 class="my-3 font-bold text-2xl">{{ products.title }}</h3>
		<p class="mb-3">{{ products.description }}</p>
		<p class="font-bold text-xl">${{ products.price }}</p>
	</div>
</template>

<script setup>
const { id } = useRoute().params;
const urlFors = "https://fakestoreapi.com/products/" + id;
const { data: products } = await useFetch(urlFors);
</script>

<style lang="scss" scoped></style>
