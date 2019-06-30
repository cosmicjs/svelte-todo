<script>
    import { createEventDispatcher } from 'svelte';

    export let todo;

    const dispatch = createEventDispatcher();

    function deleteTodo() {
        dispatch('deleteTodo', {
            todo: todo
        });
    }
    function toggleComplete() {
        dispatch('toggleComplete', {
            todo: todo
        });
    }
</script>

<style>
	.completed {
        text-decoration: line-through;
        color: grey;
    }
    .text-success {
        color:green;
    }
    .hover-cursor{
        cursor: pointer;
    }
</style>

<li class="list-group-item">
    <span class="hover-cursor {todo.metadata.is_complete ?'text-success':''}" on:click={toggleComplete}>
        <i class="fa fa-lg {todo.metadata.is_complete ?'fa-check-circle-o':'fa-circle-thin'}"></i>
    </span>
    {todo.title}
    <span class="hover-cursor text-danger pull-right" on:click={deleteTodo}>
        <i class="fa fa-trash-o fa-lg"></i>
    </span>
</li>