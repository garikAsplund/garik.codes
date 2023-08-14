<script>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';
	import { fade } from 'svelte/transition';
	export let data;
</script>
<AppShell>
	<svelte:fragment slot="header">
			<AppBar>
				<svelte:fragment slot="lead">
					<a href="/">
						<strong class="text-xl uppercase">Garik.codes</strong>
					</a>
				</svelte:fragment>
				<svelte:fragment slot="trail">
					<a
					class="btn hover:scale-110"
					href="/blog"
					>
					Blog
					</a>
					<a
					class="btn hover:scale-110"
					href="/contact"
					>
					Contact
					</a>
					<LightSwitch />
				</svelte:fragment>
			</AppBar>
		</svelte:fragment>
		{#key data.currentRoute}
		<main class="container h-full mx-auto flex justify-center items-start"
			in:fade={{ duration: 250, delay: 250 }} out:fade={{ duration: 250 }}>
		<slot />
		</main>
		{/key}
		<svelte:fragment slot="footer">
				<div class="flex flex-row justify-center gap-x-1 opacity-60">
				<a
					href="https://github.com/garikAsplund"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
				<svg class="stroke-current" xmlns="http://www.w3.org/2000/svg" width="2em" height="2em" viewBox="0 0 24 24">
					<g fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5">
						<path d="M16 22.027v-2.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7a5.44 5.44 0 0 0-1.5-3.75a5.07 5.07 0 0 0-.09-3.77s-1.18-.35-3.91 1.48a13.38 13.38 0 0 0-7 0c-2.73-1.83-3.91-1.48-3.91-1.48A5.07 5.07 0 0 0 5 5.797a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7a3.37 3.37 0 0 0-.94 2.58v2.87"/>
						<path d="M9 20.027c-3 .973-5.5 0-7-3"/>
					</g>
				</svg>
				</a>
				<a
					href="https://twitter.com/garik_law"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
				<svg class="stroke-current" fill="none" width="2em" height="2em" viewBox="0 0 48 48" id="Layer_2" data-name="Layer 2" xmlns="http://www.w3.org/2000/svg">
					<g stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5">
					<path d="M38.74,16.55v1c0,10.07-7.64,21.61-21.62,21.61A21.14,21.14,0,0,1,5.5,35.71a12.22,12.22,0,0,0,1.81.11,15.25,15.25,0,0,0,9.44-3.24,7.56,7.56,0,0,1-7.1-5.29,6.9,6.9,0,0,0,1.44.15,7.53,7.53,0,0,0,2-.27A7.57,7.57,0,0,1,7,19.72v-.1a7.42,7.42,0,0,0,3.44.94A7.54,7.54,0,0,1,8.05,10.5a21.58,21.58,0,0,0,15.68,7.94,6.38,6.38,0,0,1-.21-1.74,7.55,7.55,0,0,1,13.17-5.31,15.59,15.59,0,0,0,4.83-1.85,7.65,7.65,0,0,1-3.39,4.27,15.87,15.87,0,0,0,4.37-1.26,15.56,15.56,0,0,1-3.76,4Z"/>
					</g>
				</svg>
				</a>
				<a
					href="https://www.instagram.com/garik.asplund/"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
				<svg class="stroke-current fill-current" xmlns="http://www.w3.org/2000/svg" width="2em" height="2em" viewBox="0 0 256 256">
					<g stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5">
						<path d="M128 82a46 46 0 1 0 46 46a46.06 46.06 0 0 0-46-46Zm0 80a34 34 0 1 1 34-34a34 34 0 0 1-34 34Zm48-136H80a54.06 54.06 0 0 0-54 54v96a54.06 54.06 0 0 0 54 54h96a54.06 54.06 0 0 0 54-54V80a54.06 54.06 0 0 0-54-54Zm42 150a42 42 0 0 1-42 42H80a42 42 0 0 1-42-42V80a42 42 0 0 1 42-42h96a42 42 0 0 1 42 42ZM190 76a10 10 0 1 1-10-10a10 10 0 0 1 10 10Z"/>
					</g>
				</svg>
				</a>
				<a
					href="https://www.linkedin.com/in/garik-asplund/"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
				<svg class="stroke-current fill-current" height="2em" width="2em" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
					viewBox="0 0 45.959 45.959" xml:space="preserve">
				<g>
					<g>
						<path d="M5.392,0.492C2.268,0.492,0,2.647,0,5.614c0,2.966,2.223,5.119,5.284,5.119c1.588,0,2.956-0.515,3.957-1.489
							c0.96-0.935,1.489-2.224,1.488-3.653C10.659,2.589,8.464,0.492,5.392,0.492z M7.847,7.811C7.227,8.414,6.34,8.733,5.284,8.733
							C3.351,8.733,2,7.451,2,5.614c0-1.867,1.363-3.122,3.392-3.122c1.983,0,3.293,1.235,3.338,3.123
							C8.729,6.477,8.416,7.256,7.847,7.811z"/>
						<path d="M0.959,45.467h8.988V12.422H0.959V45.467z M2.959,14.422h4.988v29.044H2.959V14.422z"/>
						<path d="M33.648,12.422c-4.168,0-6.72,1.439-8.198,2.792l-0.281-2.792H15v33.044h9.959V28.099c0-0.748,0.303-2.301,0.493-2.711
							c1.203-2.591,2.826-2.591,5.284-2.591c2.831,0,5.223,2.655,5.223,5.797v16.874h10v-18.67
							C45.959,16.92,39.577,12.422,33.648,12.422z M43.959,43.467h-6V28.593c0-4.227-3.308-7.797-7.223-7.797
							c-2.512,0-5.358,0-7.099,3.75c-0.359,0.775-0.679,2.632-0.679,3.553v15.368H17V14.422h6.36l0.408,4.044h1.639l0.293-0.473
							c0.667-1.074,2.776-3.572,7.948-3.572c4.966,0,10.311,3.872,10.311,12.374V43.467z"/>
					</g>
				</g>
				</svg>
				</a>
			</div>
		</svelte:fragment>
</AppShell>