<script lang="ts">
    import Button from './Button.svelte'
    import Project from './project.svelte'
    import Main from './main.svelte'
	import {createEventDispatcher} from "svelte";

    let typebtn;
    function returnType(e){
       typebtn = e.detail;
       return e.detail;
    }
</script>

<main>
    <header>

        <nav class="header-container">
            <ul class="header-links">

                <li>
                    <Button on:click={returnType}></Button>
                </li>
            </ul>
        </nav>
    </header>
    {#if typebtn==='main'} <Main/> {:else} <Project/>{/if}
</main>

<style>
</style>