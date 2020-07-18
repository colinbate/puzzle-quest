<script>

export let data = [
  [1, 2, null, 4],
  [1, null, 3, 4],
  [null, 2, null, 4],
  [1, 2, null, null],
];
</script>

<style>
.crossword table, .crossword td {
  border-collapse: collapse;
  border: 1px solid #000;
}

.crossword td {
  padding: 0.25rem 0.5rem;
  background: #eee;
  color: var(--dark);
  text-align: center;
  font-size: 14px;
}

.crossword td.na {
  background: #000;
}

.puzzle table {
  margin: 0 auto;
}

</style>

<div class="puzzle clueless crossword">
  <table>
    <tbody>
    {#each data as row}
      <tr>
      {#each row as cell}
        <td class:na={cell == null}>{cell ? cell : ''}</td>
      {/each}
      </tr>
    {/each}
    </tbody>
  </table>
</div>