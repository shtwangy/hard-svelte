<script lang="ts">
  let counter = 0;
  const onClick = () => ++counter
</script>

<button on:click={onClick}>counter: {counter}</button>