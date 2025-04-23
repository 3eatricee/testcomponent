<script lang="ts">
	import { onMount } from 'svelte';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';
	import gsap from 'gsap';

	import { twMerge } from 'tailwind-merge';

	if (typeof window !== 'undefined') {
		gsap.registerPlugin(ScrollTrigger);
	}
	interface Props {
		triggerOnScroll?: boolean;
		lightCard?: string;
		darkCard?: string;
		defaultCard?: string;
	}

	let { triggerOnScroll = true, lightCard, darkCard, defaultCard }: Props = $props();

	let container: HTMLDivElement | undefined = $state();

	onMount(() => {
		if (triggerOnScroll) {
			ScrollTrigger.create({
				trigger: container,
				start: 'bottom bottom',
				end: 'bottom top',
				toggleClass: 'inView'
			});
		}
	});
</script>

<div bind:this={container} class="group relative h-[550px] w-[750px]">
	<div class="rounded-20 absolute z-0 h-full w-full">
		<div
			class={twMerge(
				'bg-primary-light absolute top-0 left-0 z-10 h-full w-full rounded-4xl transition-all duration-500 ease-[cubic-bezier(0.64,0,0.78,0)] group-[.inView]:rotate-[-7deg]',
				lightCard
			)}
		></div>
		<div
			class={twMerge(
				'bg-primary-bg border-primary-light absolute right-0 bottom-0 z-0 h-full w-full rounded-4xl transition-all duration-500 ease-[cubic-bezier(0.64,0,0.78,0)] group-[.inView]:rotate-[7deg]',
				darkCard
			)}
		></div>
	</div>
	<div
		class={twMerge(
			'bg-primary-bg shadow-offBlack/50 border-primary-muted/20 relative z-10 rounded-4xl border-[0.5px] shadow-xl',
			defaultCard
		)}
	></div>
</div>
