<script lang="ts">
  export let counter = 0;
  const onClick = () => ++counter

  $: doubled = counter * 2
  $: if (counter === 15) {
    alert(`fizzbuzz`);
    }

  const value = Math.random();

  const items = [0, 1, 2, 3];

  import Greeting from "./components/Greeting.svelte";
</script>

<button on:click={onClick}>counter: {counter}</button>
<span>double: {doubled}</span>

<div>
{#if value > 0.5}big{:else}small{/if}
</div>

{#each items as item}
  <div>{item}</div>
{/each}

<Greeting name="John" />