<script lang="ts">
const user = { loggedIn: false }

function toggle() {
  user.loggedIn = !user.loggedIn
}
</script>

<div class="app">
  {#if user.loggedIn}
    <button on:click={toggle}>Log out</button>
  {:else}
    <button on:click={toggle}>Log in</button>
  {/if}
</div>

<style>
</style>
