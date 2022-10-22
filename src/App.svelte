<script>
    import Test from './components/Test.svelte';

	let showDisplay = false;

	window.addEventListener('message', function(event) {
		let data = event.data;

		if (data.type == 'showInterface') {
			showDisplay = true;
		} else if (data.type == 'hideInterface') {
			showDisplay = false;
		}
	});
</script>

<main>
	{#if showDisplay}
		<Test/>
	{/if}
</main>