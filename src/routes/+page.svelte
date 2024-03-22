<script>
	import TestComponent from "./testComponent.svelte";
	import Counter from "./counter.svelte";
	let names =["Svelte","React","Vue"]

</script>

<TestComponent name={names[0]}></TestComponent>
<TestComponent></TestComponent>
<Counter></Counter>