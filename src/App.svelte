<script lang="ts">
  let name = 'world'
</script>

<div class="app">
  <input type="text" bind:value={name} />
  <h1>Hello {name}</h1>
</div>
