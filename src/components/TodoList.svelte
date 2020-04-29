<script>
  import TodoForm from "./TodoForm.svelte";
  import TodoRender from "./TodoRender.svelte";

  export let name;
  export let todos = [];
  export let todo = "";

  export const handleSubmit = () => {
    todos = [...todos, todo];
    todo = "";
  };

  export const handleChange = event => {
    todo = event.target.value;
  };

  export const handleDelete = index => {
    todos = todos.filter((value, i) => i !== index);
  };
</script>

<main>
  <h1>{name}'s Todos</h1>
  <TodoForm onChange={handleChange} onSubmit={handleSubmit} {todo} />
  <TodoRender onDelete={handleDelete} {todos} />
</main>
