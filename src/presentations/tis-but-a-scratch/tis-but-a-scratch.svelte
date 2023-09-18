<script>
	import Slide from '$lib/deck/slide.svelte';
	import Code from '$lib/deck/code.svelte';

	let initial_dockerfile = `FROM golang:1.21-alpine

COPY ./webapp/* .

RUN go build -o webapp

EXPOSE 8080
CMD ["./webapp"]`;
</script>

<Slide>
	<div class="flex flex-col items-start gap-44">
		<div class="flex flex-col items-start">
			<h1 class="text-4xl">’Tis But a Scratch</h1>
			<h2>
				Shrinking Containers with <code
					><span class="text-blue-500">FROM</span> scratch</code
				>
			</h2>
		</div>
		<div class="flex flex-col items-start">
			<p>Thomas Eckert</p>
			<p class="text-sm">HashiCorp</p>
		</div>
	</div>
</Slide>

<Slide>
	<div class="flex items-center justify-center">
		<Code code={initial_dockerfile} title="Dockerfile" />
	</div>
</Slide>
