<script>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';
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
					href="https://github.com/garikAsplund"
					>
					Blog
					</a>
					<LightSwitch />
				</svelte:fragment>
			</AppBar>
		</svelte:fragment>
		<slot />
		<svelte:fragment slot="footer">
				<div class="flex flex-row justify-center">
				<a
					href="https://github.com/garikAsplund"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
					<img src="github.svg" width="40" height="40" alt="GitHub"/>
				</a>
				<a
					href="https://twitter.com/garik_law"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
					<img src="twitter.svg" width="40" height="40" alt="Twitter"/>
				</a>
				<a
					href="https://www.instagram.com/garik.asplund/"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
				<img src="instagram.svg" width="40" height="40" alt="Instagram"/>
			</a>
				<a
					href="https://www.linkedin.com/in/garik-asplund/"
					target="_blank"
					rel="noreferrer"
					class="hover:scale-110"
				>
				<img src="linkedin.svg" width="40" height="40" alt="LinkedIn"/>
				</a>
			</div>
		</svelte:fragment>
</AppShell>