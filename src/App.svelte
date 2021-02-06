<script lang="ts">
  import Inner from './Inner.svelte'
</script>

<div class="app">
  <Inner on:message={(e) => alert(e.detail.text)} />
</div>
