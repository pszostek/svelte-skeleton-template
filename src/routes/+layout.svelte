<script>
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	import '@skeletonlabs/skeleton/styles/all.css';
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { Alarm, Bank, CloudMoon } from 'svelte-bootstrap-icons';
</script>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-56 p-4">
	<svelte:fragment slot="sidebarLeft">
		<!-- Insert the list: -->
		<nav class="list-nav shadow-sm">
			<ul>
				<li><a href="/">Home</a></li>
				<li><a href="/">About</a></li>
			</ul>
		</nav>
		<!-- --- -->
	</svelte:fragment>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar class="shadow-sm">
			<svelte:fragment slot="lead">
				<span class="text-base md:text-3xl font-bold uppercase">Logo</span>
			</svelte:fragment>
			<input type="search" placeholder="Search..." class="max-w-[200px]" />
			<svelte:fragment slot="trail">
				<div class="flex items-center space-x-2 container">
					<Alarm />
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
