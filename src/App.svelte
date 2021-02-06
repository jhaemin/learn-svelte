<script lang="ts">
let cats = [
  { id: 'J---aiyznGQ', name: 'Keyboard Cat' },
  { id: 'z_AbfPXTKms', name: 'Maru' },
  { id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' },
]
</script>

<div class="app">
  {#each cats as cat, i (cat)}
    <li>
      <a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">
        {i + 1}: {cat.name}
      </a>
    </li>
  {/each}
</div>

<style>
</style>
