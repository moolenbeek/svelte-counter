<script lang="ts">
	import { count } from '../stores';

	const increment = () => {
		count.update((n) => n + 1);
	};
</script>

<button type="button" class="btn-icon variant-ghost" on:click={increment}>+</button>
