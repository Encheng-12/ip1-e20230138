<template>
  <main class="wrap">
    <h1>Hello, Sokha</h1>
    <p class="muted">This is what we've got for you today.</p>
    <div class="grid">
      <section class="card"><h2>Rent received</h2><p class="price">$1,420</p><div class="bar"><div style="width:70%"></div></div></section>
      <section class="card"><h2>Unpaid invoices</h2><p class="price">3</p><span class="badge unpaid">3 unpaid</span></section>
      <section class="card"><h2>Overdue rent</h2><p class="price">$211</p><span class="badge overdue">1 overdue</span></section>
      <section class="card"><h2>Open issues</h2><p class="price">2</p><span class="badge unpaid">In progress</span></section>
    </div>
    <div class="cols">
      <section class="card">
        <div class="row"><h2>Rooms</h2><button class="btn ghost" type="button">Add room</button></div>
        <table>
          <thead><tr><th>Room</th><th>Tenant</th><th>Rent</th><th>Payment</th></tr></thead>
          <tbody>
            <tr><td>B-204</td><td>Sokha Chan</td><td>$180</td><td><span class="badge unpaid">Unpaid</span></td></tr>
            <tr><td>B-205</td><td>Dara Kim</td><td>$170</td><td><span class="badge">Paid</span></td></tr>
            <tr><td>C-101</td><td>Vacant</td><td>$200</td><td>–</td></tr>
          </tbody>
        </table>
      </section>
      <section class="card">
        <h2>Occupancy rate</h2>
        <div class="donut" style="--p:80"><span>80%</span></div>
        <p class="muted" style="text-align:center;margin:0">8 of 10 rooms occupied</p>
      </section>
    </div>
    <section class="card" style="margin-top:1rem">
      <h2>Tenant requests</h2>
      <div class="req"><div>Room B-204 · Leaking tap<small>2 Nov</small></div><span class="badge unpaid">In progress</span></div>
      <div class="req"><div>Room B-210 · Broken window<small>26 Oct</small></div><span class="badge overdue">Overdue</span></div>
    </section>
  </main>
</template>