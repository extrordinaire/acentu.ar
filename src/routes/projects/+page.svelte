<script lang="ts">
import { onMount } from 'svelte/internal';

onMount(async () => {
	await import('@material/web/button/outlined-button');
	await import('@material/web/button/text-link-button');
	await import('@material/web/iconbutton/standard-link-icon-button');
});

import Telegram from '$lib/assets/icons8-telegram-app-48.svg';
import Twitter from '$lib/assets/icons8-twitter.svg';
import Instagram from '$lib/assets/icons8-instagram.svg';
import LinkedIn from '$lib/assets/icons8-linkedin.svg';
import GitHub from '$lib/assets/icons8-github.svg';

import NavBar from '$lib/components/NavBar.svelte';
//TODO (maximo) : Create PR for documentation about --md-outlined-button-outline-width !;
</script>

<style lang="postcss">
:root {
	@apply bg-slate-50;
}

.contact > * {
	--md-icon-button-icon-size: 3rem;
	--_state-layer-size: 4rem;
}

u {
	-webkit-text-decoration-color: #f59e0b;
	text-decoration-color: #f59e0b;
	-webkit-text-decoration-style: wavy;
	text-decoration-style: wavy;
}
</style>

<div class="flex justify-center items-center w-screen">
	<section
		aria-label="Contenido principal"
		class="main flex h-screen md:max-w-7xl w-full flex-col py-10">
		<NavBar />
	</section>
</div>
