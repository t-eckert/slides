<script>
	export let title = null;
	export let code = '';
</script>

<div class={`bg-zinc-950 rounded-lg w-[40ch]`}>
	{#if title}
		<div class="text-zinc-400 text-sm border-b border-zinc-500">{title}</div>
	{/if}
	<pre><code class="text-left bg-zinc-950 rounded-lg p-2 text-sm">{code}</code></pre>
</div>
