<template>
  <main class="wrap">
    <h1>My room</h1>
    <p class="muted">Room B-204 · 12 Street 310, Phnom Penh</p>
    <div class="grid">
      <section class="card"><h2>Monthly rent</h2><p class="price">$180</p></section>
      <section class="card"><h2>Lease ends</h2><p class="price">31 Aug 2027</p></section>
      <section class="card"><h2>Next invoice</h2><p class="price">$215</p><span class="badge unpaid">Unpaid</span></section>
    </div>
    <section class="card">
      <div class="row"><h2>Recent issues</h2><button class="btn ghost" type="button">Report an issue</button></div>
      <table>
        <thead><tr><th>Title</th><th>Reported</th><th>Status</th></tr></thead>
        <tbody>
          <tr><td>Leaking tap in bathroom</td><td>2 Nov</td><td><span class="badge unpaid">In progress</span></td></tr>
          <tr><td>Broken door lock</td><td>20 Oct</td><td><span class="badge">Resolved</span></td></tr>
        </tbody>
      </table>
    </section>
  </main>
</template>