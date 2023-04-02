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
    {#each expenses as expense}
    <Expense expense={expense} />
    <!-- <Expense {...expense} /> -->
      {:else}
      <h2>Currently there are no expense</h2>
    {/each}
  </ul>
</section>