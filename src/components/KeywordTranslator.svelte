<script>
let ekey = '';
// 198.2157454488689
$: tkey = Math.floor((parseInt(ekey, 10) - 184078868902) / 198);
$: display = (!Number.isNaN(tkey) && tkey > 0) ? tkey : '';
</script>
<style>
.keyword {
  background: #000;
  color: #0f0;
  margin: 0 -1rem;
  padding: 1rem 1rem;
}

input {
  background: transparent;
  color: #fff;
  border: 0;
  border-bottom: 2px solid #fff;
}

@media (min-width: 640px) {
  .keyword {
    margin: 0 -3rem;
    padding: 1rem 3rem;
  }
}
</style>
<div class="keyword">
  <div>
    <span>Enter encoded keyword &gt;</span> <input type="text" bind:value={ekey}>
  </div>
  <div>{display}</div>
</div>