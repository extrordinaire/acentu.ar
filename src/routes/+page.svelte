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

import Card from '$lib/components/Card.svelte';
import NavBar from '$lib/components/NavBar.svelte';

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
</style>

<div class="flex h-screen w-screen items-center overflow-hidden justify-center">
	<section
		aria-label="Contenido principal"
		class="main flex h-screen md:max-w-7xl w-full flex-col py-10">
		<NavBar />

		<div class="contact my-12 flex flex-wrap items-center justify-between">
			<h1 class="font-alfa text-5xl"><u>Maximo Angel Verzini Davico</u></h1>

			<span class="icons flex flex-wrap items-center space-x-10">
				<md-standard-link-icon-button linkhref="https://linkedin.com/in/maximovv">
					<img src="{LinkedIn}" alt="LinkedIn logo." />
				</md-standard-link-icon-button>
				<md-standard-link-icon-button linkhref="https://instagram.com/maximo_avd">
					<img src="{Instagram}" alt="Instagram logo." />
				</md-standard-link-icon-button>
				<md-standard-link-icon-button linkhref="https://t.me/maximo_fsd">
					<img src="{Telegram}" alt="Telegram logo." />
				</md-standard-link-icon-button>
				<md-standard-link-icon-button linkhref="https://twitter.com/xtrordinerdev">
					<img src="{Twitter}" alt="Twitter logo." />
				</md-standard-link-icon-button>
				<md-standard-link-icon-button linkhref="https://github.com/extrordinaire">
					<img src="{GitHub}" alt="Github logo." />
				</md-standard-link-icon-button>
			</span>
		</div>

		<div class="flex w-full items-center justify-center">
			<Card
				button="??Il??strame!"
				callBack="{() => {
					console.log('pepe');
				}}"
				class="bg-rose-500">
				<h2 class="font-alfa text-4xl text-slate-50" slot="title">
					Dise??o
					<i class="material-icons" style="font-size: 2rem;">palette</i>
				</h2>
				<p class="font-fira text-xl text-slate-50">
					Planificamos la nave espacial para que se vea atractiva y sea f??cil de usar, pero sin
					comprometer la seguridad ni la funcionalidad. Ahora bien, si alg??n usuario termina
					comiendo <a href="/pochoclos" class="underline">pochoclos</a> de m??s, no podemos hacernos responsables
					de sus decisiones.
				</p>
			</Card>

			<Card
				button="??Manos a la obra!"
				callBack="{() => {
					console.log('??Manos a la obra!');
				}}"
				class="bg-amber-500">
				<h2 class="font-alfa text-4xl text-slate-50" slot="title">
					Desarrollo
					<i class="material-icons" style="{'font-size: 2rem;'}">construction</i>
				</h2>
				<p class="font-fira text-xl text-slate-50">
					Construimos una nave espacial, pero en lugar de viajar al espacio y enfrentarse a peligros
					c??smicos, llevamos al usuario en un viaje digital seguro y emocionante, ??con toda la
					diversi??n y sin espaguetizaci??n!
				</p>
			</Card>

			<Card
				button="??Ll??vame al espacio!"
				callBack="{() => {
					console.log('??Ll??vame al espacio!');
				}}"
				class="bg-teal-500">
				<h2 class="font-alfa text-4xl text-slate-50" slot="title">
					Despliegue
					<i class="material-icons" style="{'font-size: 2rem;'}">rocket_launch</i>
				</h2>
				<p class="font-fira text-xl text-slate-50">
					Enviamos una nave espacial, pero en lugar enviarla al espacio exterior, la enviamos al
					cliente, para que pueda llevar a sus usuarios en un viaje intergal??ctico desde la
					comodidad de sus casas, sin riesgos de agujeros negros ni microondas locos. ??Y s??, tambi??n
					entregamos <a href="/pochoclos" class="underline">pochoclos</a> virtuales para completar la
					experiencia!
				</p>
			</Card>
		</div>
	</section>
</div>
