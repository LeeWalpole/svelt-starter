<script>
	// import NavLeft from '$lib/components/NavLeft.svelte';
	import '../app.css';
	import NavLeft from '$lib/components/NavLeft.svelte';
	import NavBottom from '$lib/components/NavBottom.svelte';
	// import LogoWhite from '$lib/assets/logo-flames-white.webp';
	import IconFlames from '$lib/assets/icon-flames.png';
</script>

<div class="app mx-auto flex min-h-screen max-w-[1500px] text-zinc-300">
	<aside
		class="nav-left fixed left-0 top-0 hidden h-full flex-col items-center space-x-7 tablet:flex tablet:w-[120px] tablet:items-start laptop:w-[120px] desktop:w-[250px] desktop:items-start"
	>
		<NavLeft />
	</aside>
	<div class="ml-0 flex-grow tablet:ml-[120px] desktop:ml-[250px]">
		<main class="relative"><slot /></main>
	</div>
	<!-- {/* <aside className="widgets hidden laptop:flex laptop:min-w-[300px]">
	Widgets
  </aside> */} -->
</div>
<footer
	class="fixed bottom-0 left-0 flex h-[66px] w-full flex-row items-center bg-yellow-50 tablet:hidden"
>
	<NavBottom />
</footer>
