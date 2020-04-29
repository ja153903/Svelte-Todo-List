<script>
  export let onSubmit;
  export let onChange;
  export let todo;
</script>

<form on:submit|preventDefault={onSubmit}>
  <input value={todo} on:change={onChange} />
  <button type="submit">Submit</button>
</form>
