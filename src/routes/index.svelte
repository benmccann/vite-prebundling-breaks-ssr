<script>
  import Button from 'sveltestrap/src/Button.svelte';
  import Popover from 'sveltestrap/src/Popover.svelte';

  const placements = ['top', 'right', 'left', 'bottom'];
</script>

{#each placements as placement}
  <div class="mt-3">
    <Button id={`btn-${placement}`}>Click for {placement}</Button>
    <Popover
      target={`btn-${placement}`}
      {placement}
      title={`Popover ${placement}`}
    >
      This is a Popover on the {placement} of the trigger.
    </Popover>
  </div>
{/each}
