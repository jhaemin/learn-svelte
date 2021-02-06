<script lang="ts">
let count = 0
$: doubled = count * 2

$: if (count * 2 >= 10) {
  alert(`count is dangerously high! ${count}`)
  count = 5
}

function handleClick() {
  count += 1
}
</script>

<div class="app">
  <button on:click={handleClick}>
    Clicked {count}
    {count === 1 ? 'time' : 'times'}
  </button>
  <p>{count} doubled is {doubled}</p>
</div>

<style>
</style>
