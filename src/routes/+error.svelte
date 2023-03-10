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

<div class="flex w-screen items-center justify-center">
	<section
		aria-label="Contenido principal"
		class="main max-w-4/5 flex h-screen w-2/3 flex-col py-10 ">
		<NavBar />
		<div class="flex justify-center items-center mb-44 h-full">
			<h1 class="font-fira text-8xl">
				<span class="text-9xl text-rose-500 font-alfa"><u>{$page.status + ':'}</u></span>
				{$page.error?.message} :(
			</h1>
		</div>
	</section>
</div>
