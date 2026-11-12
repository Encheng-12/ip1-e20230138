<template>
  <main class="wrap">
    <h1>Invoices</h1>
    <p class="muted">Rent, water and electricity for Room B-204.</p>
    <section class="card">
      <table>
        <thead><tr><th>Month</th><th>Rent</th><th>Utilities</th><th>Total</th><th>Status</th></tr></thead>
        <tbody>
          <tr><td>November 2026</td><td>$180</td><td>$35</td><td>$215</td><td><span class="badge unpaid">Unpaid</span></td></tr>
          <tr><td>October 2026</td><td>$180</td><td>$28</td><td>$208</td><td><span class="badge">Paid</span></td></tr>
          <tr><td>September 2026</td><td>$180</td><td>$31</td><td>$211</td><td><span class="badge overdue">Overdue</span></td></tr>
        </tbody>
      </table>
    </section>
  </main>
</template>