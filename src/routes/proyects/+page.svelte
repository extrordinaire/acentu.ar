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

			<md-text-link-button href="/" data-sveltekit-preload-data="tap" label="Inicio"
			></md-text-link-button>

			<md-text-link-button href="/whoami" data-sveltekit-preload-data="tap" label="¿Quien soy?"
			></md-text-link-button>

			<u>
				<md-text-link-button href="/proyects" data-sveltekit-preload-data="tap" label="Proyectos"
				></md-text-link-button>
			</u>

			<md-text-link-button href="/contact" data-sveltekit-preload-data="tap" label="Contacto"
			></md-text-link-button>
		</nav>
	</section>
</div>
