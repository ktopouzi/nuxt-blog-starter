<script setup>
	const route = useRoute();

	const { data: article } = await useAsyncData('single-blog-post', () =>
		queryContent(route.path).findOne(),
	);

	// set the current page title and description
	useHead({
		title: article.value.title,
		meta: [
			{
				hid: 'description',
				name: 'description',
				content: article.value.description,
			},
		],
	});
</script>

<template>
	<article class="prose dark:prose-invert md:prose-xl mt-10 max-w-none">
		<ContentDoc :path="route.path" />
	</article>
</template>
