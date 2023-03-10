<script lang="ts">
interface route {
	[tag: string]: [destination: string];
}

const routes = <route>[
	{ Inicio: '/' },
	{ '¿Quien soy': '/whoami' },
	{ Proyectos: '/projects' },
	{ Contacto: '/contact' }
];
</script>

<style>
nav {
	--md-text-button-container-shape: 0.375rem;
	--md-text-button-label-text-type: 500 1.125rem/2rem Fira Sans;
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
</style>

<nav class="flex items-center space-x-10 font-fira text-lg">
	<i class="material-icons" style="font-size: 2rem;">explore</i>

	<u>
		<md-text-link-button href="/" data-sveltekit-preload-data="tap" label="Inicio"
		></md-text-link-button>
	</u>

	{#each routes as route}
		route.
	{/each}

	<md-text-link-button href="/whoami" data-sveltekit-preload-data="tap" label="¿Quien soy?"
	></md-text-link-button>

	<md-text-link-button href="/proyects" data-sveltekit-preload-data="tap" label="Proyectos"
	></md-text-link-button>

	<md-text-link-button href="/contact" data-sveltekit-preload-data="tap" label="Contacto"
	></md-text-link-button>
</nav>
