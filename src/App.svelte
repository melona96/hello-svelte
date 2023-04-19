<script>
	export let name;
    import Child from "./Child.svelte";
</script>

<main>
	<h1>I'm Parent</h1>
	
	<Child>
		<p slot="name">손흥민</p>
		<p slot="age">24</p>
		<p>속성을 정의하지 않은 Slot.</p>
	</Child>
	
</main>