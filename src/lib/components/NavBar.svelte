<script lang="ts">
import { page } from '$app/stores';
import { onMount } from 'svelte';

onMount(async () => {
	await import('@material/web/button/text-link-button');
});

interface route {
	tag: string;
	destination: string;
}

const routes: route[] = [
	{ tag: 'Inicio', destination: '/' },
	{ tag: '¿Quien soy?', destination: '/whoami' },
	{ tag: 'Proyectos', destination: '/projects' },
	{ tag: 'Contacto', destination: '/contact' }
];
</script>

<style lang="postcss">
nav {
	--md-text-button-container-shape: 0.375rem;
	--md-text-button-label-text-type: 800 1rem/1rem Fira Sans;
	--md-sys-color-primary: #0f172a;
	--md-sys-color-outline: #f1f5f9;
	--md-sys-color-on-primary: #f1f5f9;
}

u {
	-webkit-text-decoration-color: #f59e0b;
	text-decoration-color: #f59e0b;
	-webkit-text-decoration-style: wavy;
	text-decoration-style: wavy;
}

@media (min-width: 768px) {
	nav {
		--md-text-button-container-shape: 0.375rem;
		--md-text-button-label-text-type: 500 1.125rem/2rem Fira Sans;
		--md-sys-color-primary: #0f172a;
		--md-sys-color-outline: #f1f5f9;
		--md-sys-color-on-primary: #f1f5f9;
	}
}
</style>

<nav class="flex items-center md:space-x-10 md:space-x-2 font-fira">
	<i class="material-icons md:w-8 md:visible w-0 invisible" style="font-size: 2rem;">explore</i>

	<span class="flex md:flex-nowrap flex-wrap place-content-baseline">
		{#each routes as route}
			{#if $page.url.pathname === route.destination}
				<u>
					<md-text-link-button
						href="{route.destination}"
						data-sveltekit-preload-data="tap"
						label="{route.tag}"></md-text-link-button>
				</u>
			{:else}
				<md-text-link-button
					href="{route.destination}"
					data-sveltekit-preload-data="tap"
					label="{route.tag}"></md-text-link-button>
			{/if}
		{/each}
	</span>
</nav>
