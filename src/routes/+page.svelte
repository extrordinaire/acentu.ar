<script lang="ts">
import { onMount } from 'svelte/internal';

onMount(async () => {
	await import('@material/web/button/outlined-button');
	await import('@material/web/button/text-link-button');
	await import('@material/web/iconbutton/standard-link-icon-button');
});

import Telegram from '$lib/assets/Telegram.svg';
import Twitter from '$lib/assets/Twitter.svg';
import Instagram from '$lib/assets/Instagram.svg';
import LinkedIn from '$lib/assets/LinkedIn.svg';
import GitHub from '$lib/assets/GitHub.svg';
import Acentuar from '$lib/assets/favicon.svg';

import Card from '$lib/components/Card.svelte';
import NavBar from '$lib/components/NavBar.svelte';

import waves_0 from '$lib/assets/waves_0.svg';

//TODO (maximo) : Create PR for documentation about --md-outlined-button-outline-width !;
</script>

<style lang="postcss">
:root {
	@apply bg-slate-50;
}

.icons > * {
	--md-icon-button-icon-size: 3rem;
	--_state-layer-size: 4rem;
}

u {
	-webkit-text-decoration-color: #f59e0b;
	text-decoration-color: #f59e0b;
	-webkit-text-decoration-style: wavy;
	text-decoration-style: wavy;
}

b {
	@apply h-5 font-bold;
}
</style>

<div class="flex h-screen w-screen items-center justify-center overflow-hidden">
	<section
		aria-label="Contenido principal"
		class="main mt-10 flex h-screen max-w-sm flex-col px-5 md:max-w-7xl ">
		<NavBar />

		<img src="{Acentuar}" alt="acentuar logo" class="h-28" />

		<h1 class="font-alfa text-xl text-slate-900">Maximo Angel Verzini Davico</h1>

		<div
			class="flex my-8 h-12 w-auto items-center rounded-lg border-2 border-slate-900 px-5 text-lg text-slate-900">
			<i class="material-icons" style="font-size: 1.5rem;">search</i>
			<input
				type="text"
				class="flex-grow bg-transparent px-4 py-2 text-slate-900 focus:outline-0"
				placeholder="{'Search packages'}" />
			<span class="h-6 w-0.5 bg-slate-900"> </span>
			<i class="material-icons ml-5" style="font-size: 1.5rem;">tune</i>
		</div>

		<section class="grid h-full w-full max-h-40 justify-self-end">
			<div
				class="z-10 col-span-full row-span-full h-6 w-full self-start"
				style="
					background: url({waves_0}) center top repeat-x; 
				">
			</div>
			<div
				class="col-span-full row-span-full flex flex-col justify-around mt-6 h-full w-full bg-slate-800 px-6 pt-8 pb-12 text-slate-50">
				<p>
					<b>Ready, set, snap!</b> Get a good look of the awesomeness I share through my social media.
					Let's connect and sail together!
				</p>
				<section class="no-wrap flex h-full w-full flex-col items-center justify-center space-y-2">
					<span class="icons flex max-w-fit flex-wrap place-content-around items-center space-x-4">
						<md-standard-link-icon-button linkhref="https://linkedin.com/in/maximovv">
							<img src="{LinkedIn}" alt="LinkedIn logo." />
						</md-standard-link-icon-button>
						<md-standard-link-icon-button linkhref="https://instagram.com/maximo_avd">
							<img src="{Instagram}" alt="Instagram logo." />
						</md-standard-link-icon-button>
						<md-standard-link-icon-button linkhref="https://t.me/maximo_fsd">
							<img src="{Telegram}" alt="Telegram logo." />
						</md-standard-link-icon-button>
					</span>
					<span class="icons flex max-w-fit flex-wrap place-content-around items-center space-x-4">
						<md-standard-link-icon-button linkhref="https://twitter.com/xtrordinerdev">
							<img src="{Twitter}" alt="Twitter logo." />
						</md-standard-link-icon-button>
						<md-standard-link-icon-button linkhref="https://github.com/extrordinaire">
							<img src="{GitHub}" alt="Github logo." />
						</md-standard-link-icon-button>
					</span>
				</section>
				<p class="font-thin italic">Pssst... Down here got something for you</p>
			</div>
		</section>
	</section>
</div>
