<script lang="ts">
  export let counter = 0;
  const onClick = () => ++counter

  $: doubled = counter * 2
  $: if (counter === 15) {
    alert(`fizzbuzz`);
    }
</script>

<button on:click={onClick}>counter: {counter}</button>
<span>double: {doubled}</span>