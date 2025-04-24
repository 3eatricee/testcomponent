<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<div class="fixed h-screen w-full overflow-hidden">
	<div
		style="background: linear-gradient(80deg, #16181f 0%, #304064 20%, #412a60 70%, #16181f 100%)"
		class="mx-auto h-screen w-full"
	>
		<div
			class="via-primary-bg to-primary-bg h-full w-full bg-radial-[closest-side_at_50%_50%] from-transparent via-95%"
		></div>
	</div>

	<div
		class=" absolute top-[-15px] left-1/2 flex w-fit -translate-x-1/2 items-start justify-center gap-[700px]"
	>
		{#each Array(20) as _, i}
			<div class="bg-soft-grey h-[400vh] w-px origin-top-left rotate-[58deg]"></div>
		{/each}
	</div>
</div>

{@render children()}
