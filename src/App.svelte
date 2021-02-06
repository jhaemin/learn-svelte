<script lang="ts">
let m = { x: 0, y: 0 }

function handleMousemove(event: MouseEvent) {
  m.x = event.clientX
  m.y = event.clientY
}
</script>

<div class="app">
  <div on:mousemove={(e) => (m = { x: e.clientX, y: e.clientY })}>
    The mouse position is {m.x} x {m.y}
  </div>
</div>
