<script lang="ts">
	import { cn } from '$lib/utils.js';
	// import { ArrowRight } from "lucide-svelte";
	let _class: string = '';
	export { _class as class };
	export let text: string = 'Learn More';
</script>

<a
	href="/About"
	class={cn(
		'group relative rounded-full border px-6 py-3 font-semibold text-white backdrop-blur-sm transition-colors hover:bg-gray-100 hover:text-black sm:px-8',
		_class
	)}
	{...$$restProps}
>
	<span
		class="inline-block translate-x-1 transition-all duration-300 group-hover:translate-x-12 group-hover:opacity-0"
	>
		{text}
	</span>
	<div
		class="text-primary-foreground absolute top-0 z-10 flex h-full w-full translate-x-12 items-center justify-center gap-2 opacity-0 transition-all duration-300 group-hover:-translate-x-1 group-hover:opacity-100"
	>
		<span>{text}</span>
		<!-- <ArrowRight /> -->
	</div>
	<div
		class="bg-primary group-hover:bg-primary absolute left-[20%] top-[40%] h-2 w-2 scale-[1] rounded-lg transition-all duration-300 group-hover:left-[0%] group-hover:top-[0%] group-hover:h-full group-hover:w-full group-hover:scale-[1.8]"
	></div>
</a>
