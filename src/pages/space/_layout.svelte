<script>
  import { page, url, layout } from "@sveltech/routify";
  import PartNav from '~/PartNav.svelte';
  let next, prev;
  $: if ($page) next = prev = false; //reset
  $: findSiblings($page); //update buttons on page change
  function findSiblings(node) {
    prev = prev || node.prev;
    next = next || node.next;
    // make sure we have a parent and that we're not travelling past our layout
    if (node.parent && node.parent !== $layout.parent) findSiblings(node.parent);
  }
</script>

{#if prev}
  <PartNav>
  This puzzle has a <a href={$url(prev.path)}>previous part</a> that may need to be solved before this.
  </PartNav>
{/if}

<slot />

{#if next}
  <PartNav>
  This puzzle quest continues in <a href={$url(next.path)}>the next part</a>.
  </PartNav>
{/if}
