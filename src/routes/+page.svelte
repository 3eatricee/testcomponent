<script>
	import CardComponent from './components/CardComponent.svelte';
	import SquareComponent from './components/SquareComponent.svelte';
	import Map from './components/svg/map.svelte';
	import Star from './components/svg/star.svelte';
</script>

<div class="bg-primary-bg relative flex h-screen w-screen flex-col overflow-x-hidden pt-[10px]">
	<div
		class=" w-full
"
	>
		<div class="flex items-center justify-center">
			<div class="absolute left-10">
				<SquareComponent />
			</div>
			<div class="bg-soft-grey ml-[50px] h-[0.5px] w-[10%]"></div>
			<div
				class="bg-primary-light mx-4 w-fit rounded-[5px] border-[0.5px] px-[10px] py-[4px] font-mono text-[12px] leading-none font-medium text-[#0B0A11] uppercase"
			>
				who we are
			</div>
			<div class="bg-soft-grey h-[0.5px] w-[600px]"></div>

			<div class="mx-4 flex flex-col items-start gap-[4px]">
				<div class="flex items-center gap-[4px]">
					{#each Array(5) as _, i}
						<Star />
					{/each}
				</div>
				<p class=" font-mono text-[12px] font-semibold text-white uppercase">
					trusted by 500+ customers
				</p>

				<div class="z-10 row-span-2 mx-auto w-full max-w-full">
					<CardComponent />
				</div>
			</div>

			<div class="bg-soft-grey mr-[50px] h-[0.5px] grow"></div>
			<div class="absolute right-10">
				<SquareComponent />
			</div>
		</div>
	</div>

	<div>
		<div class="mt-[20px] ml-[60px] pl-[10%] font-sans">
			<div class="max-w-[400px] text-left">
				<h3 class="text-primary-light mb-[30px] text-[40px] leading-[1.2]">
					At Kalkyl, we’re perfectionists with a sense of humor that’s, well… debatable.
				</h3>
				<p class="mx-auto max-w-full text-[14px] font-light text-white">
					But when it comes to software, we leave nothing to chance. We’re here to help you rethink
					what’s possible, pushing boundaries when it makes sense – and cutting through the noise
					when it doesn’t.
				</p>
			</div>

			<div class="mt-30 flex">
				<div class="grid grid-cols-2 gap-[30px]">
					{#each Array(4) as _, i}
						<div
							class="border-border text-primary-light flex h-[80px] w-[220px] items-center justify-center rounded-sm border-1 font-mono uppercase"
						>
							Placeholder
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>

	<div
		class="px-page-border relative z-10 mt-50 flex flex-col items-center justify-center gap-[20px]"
	>
		<p class="text-14 mx-auto max-w-[385px] text-center font-sans font-light text-white">
			Our straightforward, calculated approach ensures your digital solution is exactly what it
			should be:
		</p>

		<div class="grid w-full gap-[30px] lg:grid-cols-[1fr_auto_1fr]">
			<div class="relative flex items-center">
				<div class="absolute left-10"><SquareComponent /></div>
				<div class="bg-soft-grey mr-[50px] ml-[50px] h-[0.5px] grow"></div>
				<div class="absolute right-10"><SquareComponent /></div>
			</div>
			<h4 class=" text-primary-light text-center font-sans text-[40px]">
				smart, efficient, and built for success.
			</h4>
		</div>
	</div>

	<div class="absolute right-[-10%] bottom-0 z-0 w-[70%] translate-y-[30%]">
		<Map />
	</div>
</div>
