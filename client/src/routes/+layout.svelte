
<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import factoryLogo from "$lib/images/fishfactory.png";
	
</script>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-56 p-4">
	<svelte:fragment slot="sidebarLeft">
		<!-- Insert the list: -->
		<nav class="list-nav">
			<ul>
				<li><a href="/">Home</a></li>
				<li><a href="/input">Input URL</a></li>
			</ul>
		</nav>
		<!-- --- -->
	</svelte:fragment>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<img src={factoryLogo} alt="download icon" class="w-60"/>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
		<!-- Page Route Content -->
	<slot />
</AppShell>