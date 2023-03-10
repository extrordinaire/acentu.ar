<script lang="ts">
export let callBack: Function = () => {};
export let button: string = '';
let clazz: string = '';
export { clazz as class };
import { onMount } from 'svelte/internal';

onMount(async () => {
	await import('@material/web/button/outlined-button');
	await import('@material/web/button/text-link-button');
	await import('@material/web/iconbutton/standard-link-icon-button');
});
</script>

<style>
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
</style>

<section
	class="relative my-2 mr-2 flex h-full w-full flex-col rounded-md p-6 justify-between {clazz}">
	<span>
		<h2 class="font-alfa text-4xl">
			<slot name="title" />
		</h2>
		<slot />
	</span>

	{#if button !== ''}
		<span class="flex justify-end w-full">
			<md-outlined-button on:click="{callBack}" on:keydown="{callBack}" label="{button}"
			></md-outlined-button>
		</span>
	{/if}
</section>
