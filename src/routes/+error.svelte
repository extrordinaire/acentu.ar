<script lang="ts">
import { page } from '$app/stores';
import NavBar from '$lib/components/NavBar.svelte';
import '../app.css';
</script>

<style lang="postcss">
:root {
	@apply bg-slate-50;
}

u {
	-webkit-text-decoration-color: #f59e0b;
	text-decoration-color: #f59e0b;
	-webkit-text-decoration-style: wavy;
	text-decoration-style: wavy;
}
</style>

<div class="flex h-screen w-full flex-col items-center">
	<div class="sm:my-10 px-9 w-full">
		<NavBar />
	</div>
	<div class="flex justify-center items-center h-full w-full">
		<h1 class="font-fira md:text-8xl text-6xl flex sm:flex-row flex-col">
			<span class="md:text-9xl text-7xl text-rose-500 font-alfa"><u>{$page.status + ':'}</u></span>
			{$page.error?.message} :(
		</h1>
	</div>
</div>
