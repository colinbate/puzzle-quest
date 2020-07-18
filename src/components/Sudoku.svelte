<script>

export let data = Array(9).fill(Array(9).fill(''));

</script>

<style>
.sudoku table {
  border: 5px solid #000;
  border-collapse: collapse;
}

.sudoku td {
  border-collapse: collapse;
  border: 1px solid #000;
  width: 1.2rem;
  height: 1.2rem;
  text-align: center;
}

.sudoku tr:nth-child(3n+1) {
  border-top: 3px solid #000;
}

.sudoku td:nth-child(3n+1) {
  border-left: 3px solid #000;
}

.sudoku td {
  padding: 0.75rem 0.9rem;
  background: #eee;
  color: var(--dark);
}

.sudoku td.b,
.sudoku td.x {
  background: #bee;
}

.sudoku td.y,
.sudoku td.x {
  background-image: radial-gradient(circle, transparent 0%, transparent 67%, rgba(139,139,139,1) 67%, rgba(139,139,139,1) 100%)
}

.puzzle table {
  margin: 0 auto;
}

</style>

<div class="puzzle sudoku">
  <table>
    <tbody>
    {#each data as row}
      <tr>
      {#each row as cell}
        <td class={cell && cell.type ? cell.type : ''}>{@html cell && cell.num ? cell.num : '&nbsp;'}</td>
      {/each}
      </tr>
    {/each}
    </tbody>
  </table>
</div>