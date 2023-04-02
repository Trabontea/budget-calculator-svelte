<script>
  import {getContext} from 'svelte'
  export let expense;
  let {id, name, amount} = expense;
  console.log(id)
  // export let name='';
  // export let amount=0;
  let displayAmount = false;
  // Add a function
  function toggleAmount() {
    displayAmount = !displayAmount;
  }

  //get context
  const removeExpense = getContext('remove');
</script>

<article class="single-expense">
  <div class="expense-info">
    <h2>
      <span>{name}</span>
      <button class="amount-btn" on:click|once="{toggleAmount}">
        <i class="fas fa-caret-down"></i>
      </button>
    </h2>
    {#if displayAmount}
      <h4>amount: ${amount}</h4>
    {/if}
  </div>
  <div class="expense-buttons">
    <button class="expense-btn edit-btn">
      <i class="fas fa-pen"></i>      
    </button>
    <button class="expense-btn delete-btn" on:click={() => removeExpense(id)}>
      <i class="fas fa-trash" />

    </button>
  </div>
</article>
