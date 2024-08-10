<script lang="ts">
	import { count } from '../stores';
	import Incrementer from '$lib/Incrementer.svelte';
	import Decrementer from '$lib/Decrementer.svelte';

	let countValue: number;

	count.subscribe((value) => {
		countValue = value;
	});
</script>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="space-y-5">
		<h1>The count is: {countValue}</h1>
		<Incrementer />
		<Decrementer />
	</div>
</div>
