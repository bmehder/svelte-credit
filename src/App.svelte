<script>
  const formatter = new Intl.NumberFormat("en-US", {
    style: "currency",
    currency: "USD"
  });
  let loanAmount = 200000;
  let years = 15;
  let interestRateInput = 200;

<<<<<<< HEAD
  $: months = (loanAmount / monthlyPaymentInput).toFixed(1);
=======
>>>>>>> parent of 00b1465... Fixed horizontal scroll on mobile
  $: interestRate = interestRateInput / 100;
  $: totalPayments = years * 12;
  $: monthlyInterestRate = interestRate / 100 / 12;
  $: monthlyPayment =
    (loanAmount *
      Math.pow(1 + monthlyInterestRate, totalPayments) *
      monthlyInterestRate) /
    (Math.pow(1 + monthlyInterestRate, totalPayments) - 1);

  $: totalPaid = monthlyPayment * totalPayments;
  $: interestPaid = totalPaid - loanAmount;
</script>

<style>
  .outputs {
    background: #0073ff;
    margin-top: 15px;
    padding: 0.5em;
    border-radius: 4px;
    font-size: 20px;
    text-align: center;
    color: white;
  }
  .outputs.settings {
    background-color: darkorange;
<<<<<<< HEAD
    justify-content: center;
  }
  .outputs p {
    width: 50%;
    margin-bottom: 0;
=======
>>>>>>> parent of 00b1465... Fixed horizontal scroll on mobile
  }
  .controls {
    margin-top: 1em;
  }
</style>

<main class="container">
  <div class="row">
<<<<<<< HEAD
    <h1>Credit Cardulator</h1>
=======
    <h1>Mortgage Calculator</h1>
>>>>>>> parent of 00b1465... Fixed horizontal scroll on mobile
  </div>
  <div class="row">
    <label>Loan Amount</label>
    <input
      class="u-full-width"
      min="1"
      type="number"
      bind:value={loanAmount}
      placeholder="Enter loan amount..." />
  </div>

  <div class="row">
<<<<<<< HEAD
    <div class="columns six outputs settings">{months} months</div>
    <div class="columns six outputs settings">{interestRate.toFixed(2)} %</div>
  </div>

  <div class="row outputs">
    <p>Payments:</p>
    <p>{formatter.format(monthlyPaymentInput)}</p>
  </div>
  <div class="row outputs">
    <p>Total Paid:</p>
    <p>{formatter.format(totalPaid)}</p>
  </div>
  <div class="row outputs">
    <p>Interest Paid:</p>
    <p>{formatter.format(interestPaid)}</p>
  </div>

  <div class="row controls">

    <div class="columns four">
      <label>Monthly Payments</label>
      <input
        type="range"
        class="u-full-width years"
        min="1"
        max={loanAmount}
        bind:value={monthlyPaymentInput} />
    </div>

    <div class="columns four">
      <label>Months</label>
=======
    <div class="columns six">
      <label>Years</label>
>>>>>>> parent of 00b1465... Fixed horizontal scroll on mobile
      <input
        type="range"
        class="u-full-width years"
        min="1"
        max="50"
<<<<<<< HEAD
        bind:value={months} />
=======
        bind:value={years} />
>>>>>>> parent of 00b1465... Fixed horizontal scroll on mobile
    </div>

    <div class="columns four">
      <label>Interest Rate</label>
      <input
        type="range"
        class="u-full-width years"
        min="1"
        max="2000"
        bind:value={interestRateInput} />
    </div>

  </div>
<<<<<<< HEAD
=======
  <div class="row">
    <div class="columns six outputs settings">{years} years</div>
    <div class="columns six outputs settings">{interestRate.toFixed(2)} %</div>
  </div>

  <div class="row outputs">
    Monthly Payments: {formatter.format(monthlyPayment)}
  </div>
  <div class="row outputs">Total Paid: {formatter.format(totalPaid)}</div>
  <div class="row outputs">Interest Paid: {formatter.format(interestPaid)}</div>
>>>>>>> parent of 00b1465... Fixed horizontal scroll on mobile

</main>
