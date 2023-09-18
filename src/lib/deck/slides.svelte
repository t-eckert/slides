<script>
	import { onMount } from 'svelte';

	import Reveal from 'reveal.js';
	import Markdown from 'reveal.js/plugin/markdown/markdown';
	import Hightlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';

	onMount(() => {
		const deck = new Reveal();

		deck.initialize({
			plugins: [Markdown, Hightlight, Notes]
		});
	});
</script>

<div class="reveal">
	<div class="slides theme">
		<slot />
	</div>
</div>
