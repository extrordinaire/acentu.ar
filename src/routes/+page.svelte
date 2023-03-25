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
import SearchBar from '$lib/components/SearchBar.svelte';

import waves_0 from '$lib/assets/waves_0.svg';
import waves_1 from '$lib/assets/waves_1.svg';
import waves_3 from '$lib/assets/waves_3.svg';
import waves_6 from '$lib/assets/waves_6.svg';
import waves_8 from '$lib/assets/waves_8.svg';

//TODO (maximo) : Create PR for documentation about --md-outlined-button-outline-width !;
</script>

<style lang="postcss">
:root {
	@apply m-0 bg-slate-50 p-0 text-slate-900;
}

.icons > * {
	--md-icon-button-icon-size: 3rem;
	--md-icon-button-state-layer-size: 4rem;
}

b {
	@apply h-5 font-bold;
}
</style>

<div class="flex h-screen w-full flex-col items-center">
	<div class="sm:my-10 px-9 w-full">
		<NavBar />
	</div>
	<section class="flex w-full basis-full flex-col justify-between space-y-10">
		<div class="flex flex-col space-y-4 basis-full justify-evenly">
			<img src="{Acentuar}" alt="Acentuar logo." class="self-center" />
			<h1 class="self-center font-alfa text-xl">Maximo Angel Verzini Davico</h1>
			<h2 class="flex items-center self-center font-fira text-lg">
				Semi-senior Full-Stack developer <span
					class="material-icons select-none text-amber-400 ml-2"
					style="font-size: 1rem;">favorite</span>
			</h2>
		</div>
		<div class="w-full px-9 pb-10">
			<SearchBar />
		</div>
	</section>
	<section class="h-full w-full">
		<div class="relative grid h-full">
			<div
				style="background: url({waves_0});"
				class="relative -top-6 col-span-full row-span-full h-7 bg-repeat-x">
			</div>
			<div
				class="icons col-span-full row-span-full h-full bg-slate-800 px-9 py-12 text-slate-50 flex flex-col justify-evenly items-center">
				<p>
					<b>Ready, set, shine!</b> Get a good look of the awesomeness I share through my social media.
					Let's connect and sail together!
				</p>

				<div class="flex flex-col space-y-3">
					<div class="flex justify-center space-x-8">
						<md-standard-link-icon-button linkhref="https://t.me/Maximo_fsd" linktarget="_blank">
							<img src="{Telegram}" alt="telegram logo" />
						</md-standard-link-icon-button>
						<md-standard-link-icon-button
							linkhref="https://www.instagram.com/maximo_avd/"
							linktarget="_blank">
							<img src="{Instagram}" alt="instagram logo" />
						</md-standard-link-icon-button>
						<md-standard-link-icon-button
							linkhref="https://twitter.com/xtrordinerdev"
							linktarget="_blank">
							<img src="{Twitter}" alt="twitter" />
						</md-standard-link-icon-button>
					</div>
					<div class="flex justify-center space-x-8">
						<md-standard-link-icon-button
							linkhref="https://github.com/extrordinaire"
							linktarget="_blank">
							<img src="{GitHub}" alt="github" />
						</md-standard-link-icon-button>
						<md-standard-link-icon-button
							linkhref="https://github.com/extrordinaire"
							linktarget="_blank">
							<img src="{LinkedIn}" alt="linked_in" />
						</md-standard-link-icon-button>
					</div>
				</div>
				<i>Pssst... Down here got something for you</i>
			</div>
		</div>
	</section>
</div>
<div class="flex h-screen w-full flex-col items-center">
	<section class="h-full w-full basis-full">
		<div class="relative grid h-1/2">
			<div
				style="background: url({waves_1});"
				class="relative -top-6 col-span-full row-span-full h-6 bg-repeat-x">
			</div>
			<div class="col-span-full row-span-full h-full bg-rose-500 px-9 py-12 text-slate-50">
				<b>Flirtatious and original</b>, we design spaceships sexy and easy to use, with no
				compromise on safety nor function. But if you eat too much <u>pochoclo</u> from the sheer awesomeness
				of it all, we won’t held responsible.
			</div>
		</div>
		<div class="relative grid h-1/2">
			<div
				style="background: url({waves_3});"
				class="relative -top-6 col-span-full row-span-full h-6 bg-repeat-x">
			</div>
			<div class="col-span-full row-span-full h-full bg-amber-500 px-9 py-12 text-slate-50">
				<b>Rock solid and innovative</b>, we code our products with the highest standards and
				conventions, ensuring unbeatable security, sturdiness, and reliability. Experience a safe
				and thrilling digital journey, with no risk of cosmic disasters or spaghetti-fication!
			</div>
		</div>
		<div class="relative grid h-1/2">
			<div
				style="background: url({waves_6});"
				class="relative -top-6 col-span-full row-span-full h-6 bg-repeat-x">
			</div>
			<div class="col-span-full row-span-full h-full bg-teal-500 px-9 py-12 text-slate-50">
				<b>Launching, batteries included</b>, we deliver out-of-this-world experiences that take the
				users into a completely seamless experience without leaving their homes (yes, without any
				background microwave radiation, nor black holes) in a completely safe way!
			</div>
		</div>
		<div class="relative grid h-full">
			<div
				style="background: url({waves_8});"
				class="relative -top-6 col-span-full row-span-full h-6 bg-repeat-x">
			</div>
			<div class="col-span-full row-span-full h-full bg-slate-900 px-9 py-12 text-slate-50">
				<b>Launching, batteries included</b>, we deliver out-of-this-world experiences that take the
				users into a completely seamless experience without leaving their homes (yes, without any
				background microwave radiation, nor black holes) in a completely safe way!
			</div>
		</div>
	</section>
</div>
