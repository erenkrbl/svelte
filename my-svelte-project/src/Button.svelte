<script>
    export let show = false;
    export let success = false;

</script>
<style>
    .danger {
        background-color: red;
        color:white;
        border: none;
        border-radius: 10px;
    }
    .success {
        background-color:green;
        color:white;
        border: none;
        border-radius: 10px;
    }

</style>
{#if show}
<button class = {success ? "success" : "danger"}>Click Me!</button>{/if}