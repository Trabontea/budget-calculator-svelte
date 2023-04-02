<script>
  // components
  import Navbar from "../components/Navbar.svelte";
  import ExpensesList from "../components/ExpensesList.svelte";
  import { setContext } from 'svelte';

  // data
  import expensesData from '../data/expenses.js'
  // variables // add the data in a local variable
  let expenses = [...expensesData];
  console.log(expenses)

  //functions
  function removeExpense(id) {
  expenses = expenses.filter(item => 
      item.id !== id
    );
  }

  // context
  setContext('remove', removeExpense)
</script>

<!-- Template -->
<Navbar />
<main class="content">
  <div class="container">
    <ExpensesList {expenses}/>
  </div>
</main>
<svelte:head>
    <title>Budget Application</title>
</svelte:head>

