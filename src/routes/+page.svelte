<script>
  // components
  import Navbar from "../components/Navbar.svelte";
  import ExpensesList from "../components/ExpensesList.svelte";

  // data
  import expensesData from '../data/expenses.js'
  // variables
  let expenses = [...expensesData];
  console.log(expenses)

  //functions
</script>

<!-- Template -->
<Navbar />
<main class="content">
  <div class="container">
    <ExpensesList  {expenses} />
  </div>
</main>
<svelte:head>
    <title>Home</title>
</svelte:head>

