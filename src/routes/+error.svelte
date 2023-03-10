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

<div class="flex w-screen h-screen overflow-clip items-center justify-center">
	<section
		aria-label="Contenido principal"
		class="main flex h-screen md:max-w-7xl w-full flex-col py-10">
		<NavBar />
		<div class="flex justify-center items-center h-full">
			<h1 class="font-fira md:text-8xl text-6xl">
				<span class="md:text-9xl text-7xl text-rose-500 font-alfa"
					><u>{$page.status + ':'}</u></span>
				{$page.error?.message} :(
			</h1>
		</div>
	</section>
</div>
