<script lang="ts">
    import {createEventDispatcher} from "svelte";
    const dispatch = createEventDispatcher();
</script>

<button on:click = {()=>dispatch('click', 'main')}>
    <slot></slot> HOME
</button>
<button on:click = {()=>dispatch('click', 'project')}>
    <slot></slot>PROJECT
</button>