<script>
	$: wish = '';
	$: wished = false;
	export const submit = () => {
		wish = '';
		wished = true;

		setTimeout(() => {
			wished = false;
		}, 5000);
	};
</script>

<h1>Fungalore</h1>
<h2>He heard your wish.</h2>

<p>
	Take a moment to compose a wish. When you are ready, close your eyes and hit "submit" or "Enter".
</p>

{#if wished}
	<h3>Heard, Chef.</h3>
{:else}
	<input type="text" bind:value={wish} />
	<button on:click={submit}>Submit</button>
{/if}

<p>This text of these wishes are not saved, stored, or transmitted.</p>
<p>Wishes made will be heard by Fungalore, be they here or elsewhere.</p>
<p>This is merely an opportunity to reflect on your needs and the needs of y our community.</p>
