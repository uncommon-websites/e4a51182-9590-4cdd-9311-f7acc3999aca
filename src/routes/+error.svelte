<script lang="ts">
	import { page } from "$app/state";
</script>

<main class="min-h-screen bg-[#050505] flex items-center justify-center px-4">
	<div class="text-center">
		<h1 class="text-6xl font-bold text-white mb-4">Error {page.status}</h1>
		<p class="text-gray-400 mb-8 text-lg">{page.error?.message ?? "Something went wrong."}</p>
		<a href="/" class="bg-white text-black px-6 py-3 rounded-full font-semibold hover:bg-gray-200 transition-colors inline-block">Go back home</a>
	</div>
</main>
