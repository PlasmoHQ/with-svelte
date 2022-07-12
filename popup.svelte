<script lang="ts">
    export let count = 0;
    let action: string = null;
    function increment() {
        count += 1;
        action = "increment";
    }
    function decrement() {
        count -= 1;
        action = "decrement";
    }
</script>

<style>
    .container {
        min-width: 470px;
    }
    .action {
        color: #470;
        font-weight: bold;
    }
</style>

<div class="container">
    <p>Current count: <b>{count}</b></p>
    <div>
        <button on:click={decrement}>-</button>
        <button on:click={increment}>+</button>
        {#if action}<span class="action">{action}</span>{/if}
    </div>
</div>
