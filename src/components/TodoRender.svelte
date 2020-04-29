<script>
  export let onDelete;
  export let todos;
</script>

<ul>
  {#each todos as todo, i}
    <li on:click={() => onDelete(i)}>{todo}</li>
  {/each}
</ul>
