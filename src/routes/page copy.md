<script lang="ts">
    const greetingOject = {
        greeting: "hello",
        hello: "world"
    }
    const data = {
        "yellow",
        "red",
        "blue",
    }
</script>

<h1>Welcome to {hello} {hi}</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

{#each data as color, 1 (color)}
<div>
    {1+1}; {color}
</div>


<style>
 h1{
    color: red
 }
</style>

