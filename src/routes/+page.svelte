<script>
	import CardComponent from '../lib/components/CardComponent.svelte';
	import SquareComponent from '../lib/components/SquareComponent.svelte';
	import Map from '../lib/components/svg/map.svelte';
</script>

<div class="relative flex h-screen w-screen flex-col overflow-x-hidden pt-[10px]">
	<div class="w-full">
		<div class="flex items-center justify-center">
			<div class="absolute left-5 xl:left-10">
				<SquareComponent />
			</div>
			<div
				class="bg-soft-grey absolute bottom-0 left-[31px] h-full w-[0.5px] translate-x-[-50%] xl:left-[51px]"
			></div>

			<div class="bg-soft-grey ml-[31px] h-[0.5px] grow lg:max-w-[10%] xl:ml-[51px]"></div>
			<div
				class="bg-primary-light mx-4 w-fit rounded-[5px] border-[0.5px] px-[10px] py-[4px] font-mono text-[12px] leading-none font-medium uppercase"
			>
				who we are
			</div>
			<div class="bg-soft-grey h-[0.5px] grow"></div>

			<div class="absolute right-5 xl:right-10">
				<SquareComponent />
			</div>
			<div
				class="bg-soft-grey absolute right-[31px] bottom-0 h-full w-[0.5px] translate-x-[-50%] xl:right-[51px]"
			></div>
		</div>
	</div>

	<div
		class="xs:mr-[27px] xs:ml-[27px] mt-[20px] flex justify-center font-sans lg:mr-[60px] lg:ml-[60px] lg:justify-start lg:pr-[0%] lg:pl-[0%] xl:pr-[10%] xl:pl-[10%]"
	>
		<div class="grid grid-cols-1 items-start gap-[60px] lg:grid-cols-2">
			<div class="flex flex-col gap-[40px]">
				<div class="max-w-[500px] text-center lg:text-left">
					<h3
						class="text-primary-light xs:text-[20px] mb-[30px] leading-[1.2] lg:text-[30px] xl:text-[40px]"
					>
						At Kalkyl, we’re perfectionists with a sense of humor that’s, well… debatable.
					</h3>
					<p class="text-[14px] font-light text-white">
						But when it comes to software, we leave nothing to chance. We’re here to help you
						rethink what’s possible, pushing boundaries when it makes sense – and cutting through
						the noise when it doesn’t.
					</p>

					<div class="flex justify-center pt-20 lg:justify-start">
						<div class="xs:gap-[10px] grid grid-cols-2 xl:gap-[30px]">
							{#each Array(4) as _, i}
								<div
									class="border-border text-primary-light xs:h-[72px] xs:w-[170px] xs:text-[10px] flex items-center justify-center rounded-sm border-1 font-mono uppercase lg:text-[12px] xl:h-[80px] xl:w-[220px]"
								>
									Placeholder
								</div>
							{/each}
						</div>
					</div>
				</div>
			</div>

			<div class="z-10 flex justify-center pt-[50px]">
				<CardComponent
					lightCard=" group-[.inView]:rotate-[-5deg]"
					defaultCard="w-full h-full overflow-hidden"
				/>
			</div>
		</div>
	</div>

	<div
		class="px-page-border xs:mt-[50px] relative z-10 flex flex-col items-center justify-center gap-[20px] lg:mt-[100px]"
	>
		<p class="text-14 mx-auto max-w-[385px] text-center font-sans font-light text-white">
			Our straightforward, calculated approach ensures your digital solution is exactly what it
			should be:
		</p>

		<div class="grid w-full gap-[30px] lg:grid-cols-[1fr_auto_1fr]">
			<div class=" relative hidden items-center lg:flex">
				<div class="absolute left-5 xl:left-10"><SquareComponent /></div>
				<div
					class="bg-soft-grey mr-[31px] ml-[30px] h-[0.5px] grow xl:mr-[50px] xl:ml-[51px]"
				></div>
				<div class="absolute right-5 xl:right-10"><SquareComponent /></div>
			</div>
			<h4 class="text-primary-light xs:text-[26px] text-center font-sans xl:text-[40px]">
				smart, efficient, and built for success.
			</h4>
		</div>
	</div>

	<div
		class="absolute right-[-10%] bottom-0 z-0 hidden w-[70%] sm:translate-y-[-30%] lg:block lg:translate-y-[-20%] xl:translate-y-[10%]"
	>
		<Map />
	</div>
</div>
