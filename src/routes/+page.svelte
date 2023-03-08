<script lang="ts">
import '@material/web/button/outlined-button';
import '@material/web/button/text-link-button';
import '@material/web/iconbutton/standard-link-icon-button';

import Telegram from '$lib/assets/icons8-telegram-app-48.svg';
import Twitter from '$lib/assets/icons8-twitter.svg';
import Instagram from '$lib/assets/icons8-instagram.svg';
import LinkedIn from '$lib/assets/icons8-linkedin.svg';
import GitHub from '$lib/assets/icons8-github.svg';

//TODO (maximo) : Create PR for documentation about --md-outlined-button-outline-width !;
</script>

<style lang="postcss">
:root {
	@apply bg-slate-50;
}

nav {
	--md-text-button-container-shape: 0.375rem;
	--md-text-button-label-text-type: 500 1.125rem/2rem Fira Sans;
	--md-sys-color-primary: #0f172a;
	--md-sys-color-outline: #f1f5f9;
	--md-sys-color-on-primary: #f1f5f9;
}

section {
	--md-outlined-button-container-shape: 0.375rem;
	--md-outlined-button-label-text-type: 500 1.25rem/2rem Fira Sans;
	--md-sys-color-primary: #f8fafc;
	--md-sys-color-outline: #f8fafc;
	--md-sys-color-on-primary: #f8fafc;
	--md-outlined-button-outline-width: 4px;
	--md-outlined-button-spacing-leading: 50px;
	--md-outlined-button-spacing-trailing: 50px;
	--md-outlined-button-container-height: 60px;
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
		class="main flex flex-col h-screen max-w-4/5 w-2/3 py-10 ">
		<nav class="flex items-center space-x-10 font-fira text-lg">
			<i class="material-icons" style="font-size: 2rem;">explore</i>

			<u>
				<md-text-link-button href="/" data-sveltekit-preload-data="tap" label="Inicio"
				></md-text-link-button>
			</u>

			<md-text-link-button href="/whoami" data-sveltekit-preload-data="tap" label="¿Quien soy?"
			></md-text-link-button>

			<md-text-link-button href="/proyects" data-sveltekit-preload-data="tap" label="Proyectos"
			></md-text-link-button>

			<md-text-link-button href="/contact" data-sveltekit-preload-data="tap" label="Contacto"
			></md-text-link-button>
		</nav>

		<div class="contact flex items-center space-x-10 my-12">
			<h1 class="font-alfa text-5xl"><u>Maximo Angel Verzini Davico</u></h1>

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
		</div>

		<div class="flex w-full items-center justify-center">
			<div class="grid grid-cols-3">
				<section class="relative my-2 mr-2 flex flex-col rounded-md bg-rose-500 p-6">
					<h2 class="font-alfa text-4xl text-slate-50">
						Diseño
						<i class="material-icons" style="font-size: 2rem;">palette</i>
					</h2>

					<p class="font-fira text-xl text-slate-50">
						Planificamos la nave espacial para que se vea atractiva y sea fácil de usar, pero sin
						comprometer la seguridad ni la funcionalidad. Ahora bien, si algún usuario termina
						comiendo <a href="/pochoclos" class="underline">pochoclos</a> de más, no podemos hacernos
						responsables de sus decisiones.
					</p>

					<md-outlined-button
						on:click="{() => {
							console.log('¡Ilústrame!');
						}}"
						label="¡Ilústrame!"
						class="absolute right-6 bottom-6"></md-outlined-button>
				</section>
				<section
					class="relative my-2 mr-1 ml-1 flex aspect-square flex-col rounded-md bg-amber-500 p-6">
					<h2 class="font-alfa text-4xl text-slate-50">
						Desarrollo
						<i class="material-icons" style="font-size: 2rem;">construction</i>
					</h2>
					<p class="font-fira text-xl text-slate-50">
						Construimos una nave espacial, pero en lugar de viajar al espacio y enfrentarse a
						peligros cósmicos, llevamos al usuario en un viaje digital seguro y emocionante, ¡con
						toda la diversión y sin espaguetización!
					</p>

					<md-outlined-button
						on:click="{() => {
							console.log('¡Manos a la obra!');
						}}"
						label="¡Manos a la obra!"
						class="absolute right-6 bottom-6"></md-outlined-button>
				</section>
				<section class="relative my-2 ml-2 flex flex-col rounded-md bg-teal-500 p-6">
					<h2 class="font-alfa text-4xl text-slate-50">
						Despliegue
						<i class="material-icons" style="{'font-size: 2rem;'}">rocket_launch</i>
					</h2>
					<p class="font-fira text-xl text-slate-50">
						Enviamos una nave espacial, pero en lugar enviarla al espacio exterior, la enviamos al
						cliente, para que pueda llevar a sus usuarios en un viaje intergaláctico desde la
						comodidad de sus casas, sin riesgos de agujeros negros ni microondas locos. ¡Y sí,
						también entregamos <a href="/pochoclos" class="underline">pochoclos</a> virtuales para completar
						la experiencia!
					</p>

					<md-outlined-button
						on:click="{() => {
							console.log('¡Llévame al espacio!');
						}}"
						label="¡Llévame al espacio!"
						class="absolute right-6 bottom-6"></md-outlined-button>
				</section>
			</div>
		</div>
	</section>
</div>
