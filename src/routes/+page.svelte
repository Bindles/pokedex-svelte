<script lang="ts">
    const greetingOject = {
        greeting: "hello",
        hello: "world"
    }
    const colordata = [
        "yellow",
        "red",
        "blue",
]
    
    import {hello} from './export'
    import {generations} from './generations'
    let monsters =[
        {"name":"bulbasaur","url":"https://pokeapi.co/api/v2/pokemon/1/"},{"name":"ivysaur","url":"https://pokeapi.co/api/v2/pokemon/2/"},{"name":"venusaur","url":"https://pokeapi.co/api/v2/pokemon/3/"},
    ]
    fetch('https://pokeapi.co/api/v2/pokemon?limit=151')
    .then(response => response.json())
    .then(data =>{
        monsters = data.results
    })
</script>

{#each monsters as mon}
    <h1>{mon.name}</h1>
{/each}

{#each generations as gen}
    <h1>{gen.name}</h1>
    <p>{gen.games.join(', ')}</p>
    <p>{gen.main_region}</p>
{/each}


{hello}<br>
{greetingOject.greeting} {greetingOject.hello}

{#each colordata as color, iter (color)}
<div>
    {iter}: {color}
</div>
{/each}


<style>
 h1{
    color: red
 }
</style>

