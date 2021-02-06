<script lang="ts">
async function getRandomNumber() {
  const res = await fetch(`tutorial/random-number`)
  const text = await res.text()

  if (res.ok) {
    return text
  } else {
    throw new Error(text)
  }
}

let promise = getRandomNumber()

function handleClick() {
  promise = getRandomNumber()
}
</script>

<div class="app">
  <button on:click={handleClick}>generate random number</button>

  {#await promise}
    <p>...waiting</p>
  {:then number}
    <p>The number is {number}</p>
  {:catch error}
    <p style="color: red">error</p>
  {/await}
</div>
