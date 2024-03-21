<script>
    export let items;
    let target=0;
    function toggle(){
        const nextTarget = Math.floor(Math.random()*items.length+1);
        if(nextTarget===target){
            toggle()
        } else {
            target = nextTarget
        }
    }
</script>
<div class="wrapper">
<ul class="run" style="--target: {target}">
    <!-- I know, ikke click på li -->
    <li on:click={toggle}>???</li>
    {#each items as item}
        <li on:click={toggle}>{item}</li>
    {/each}
</ul>
</div>
<style>
    div.wrapper {
        display:inline-block;
        height:calc(var(--base-size)*2 + 1px);
        overflow:hidden;
        vertical-align:bottom;
    }
    ul {
        list-style: none;
        vertical-align:bottom;
    }
    li {
        padding-top: var(--base-size);
        border-bottom:1px solid hotpink;
        text-align:center;
        cursor:pointer;
    }
    li:hover {
        color:hotpink;
    }
    
    .run {
        transition: all 1s;
        transform:translateY(calc(var(--target) * var(--base-size) * -2 + var(--target) * -1px));
    }
</style>