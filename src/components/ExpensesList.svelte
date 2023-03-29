<script>
  import SectionTitle from "./Title.svelte";
  import Expense from "./Expense.svelte";
  export let expenses = [];

</script>

<style>
  h2 {
    text-transform: capitalize;
  }
</style>

<section>
  <SectionTitle  title="expenses list"/>
  <ul>
    {#each expenses as expense, index}
    <Expense expense={expense} index={index + 1}/>
    <!-- <Expense {...expense} /> -->
      {:else}
      <h2>Currently there are no expense</h2>
    {/each}
  </ul>
</section>