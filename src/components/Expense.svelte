<script>
  export let expense;
  let {name, amount} = expense
  export let index = '';
  // export let name='';
  // export let amount=0;
</script>

<article class="single-expense">
<div class="expense-info">
  <h2>
    <span>{name}</span>
    <button class="amount-btn">
      <i class="fas fa-caret-down"></i>
    </button>
  </h2>
  <h4>amount: ${amount}</h4>
</div>
<div class="expense-buttons">
  <button class="expense-btn edit-pen">
    <i class="fas fa-pen"></i>      
  </button>
  <button class="expense-btn delete-pen">
    <i class="fas fa-trash"></i>      
  </button>
</div>
</article>
