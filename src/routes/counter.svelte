<script>
    let numbers = [1];
    let count = 0;
    //reactive declaration
    $: doubled = count *2;
    $: console.log(`The count is ${count}`)
    $: if (count >= 10) {
	alert('count is dangerously high!');
	count = 0;
    }

    function counter(){
        count += 1;
        }
// Using array in function need to add assignment that would otherwise be redundant numbers = numbers to update reactivity
    function addNumber() {
    numbers.push(numbers.length + 1);
    numbers = numbers;
}
console.log(numbers);
</script>

<button on:click={counter} on:click={addNumber}>
	Clicked {count}

	{count === 1 ? 'time' : 'times'}
</button>
{#if count >= 5}
<p>The count increaded to {count}</p>
{/if}
<p>{count} doubled is {doubled}</p>
<p>{numbers}</p>

{#if count > 5}
	<p>{count} is greater than 5</p>
    {:else}
    <p>{count} is below 5</p>
{/if}


<style>


</style>