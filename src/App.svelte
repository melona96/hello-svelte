<script>
	export let name;
    import Child from "./Child.svelte";
    import LifeCycle from "./LifeCycle.svelte";
	import { onMount, onDestroy, beforeUpdate, afterUpdate, tick } from 'svelte';

	onMount(async() => {
		console.log('App onMount')
	})

	onDestroy(async() => {
		console.log('App onDestroy')
	})

	beforeUpdate(async() => {
	console.log('App beforeUpdate') 
	})

	afterUpdate(async() => {
		console.log('App afterUpdate')
	})

</script>

<main>
	<h1>I'm Parent</h1>
	<LifeCycle>
	</LifeCycle>
	
	<Child>
		<p slot="name">손흥민</p>
		<p slot="age">24</p>
		<p>속성을 정의하지 않은 Slot.</p>
	</Child>
	
</main>