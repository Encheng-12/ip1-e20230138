<template>
  <main class="wrap">
    <h1>Report an issue</h1>
    <p class="muted">Tell your landlord what needs fixing.</p>
    <section class="card">
      <label for="title">Title</label>
      <input id="title" placeholder="Leaking tap in bathroom" />
      <label for="category">Category</label>
      <select id="category"><option>Plumbing</option><option>Electrical</option><option>Furniture</option><option>Other</option></select>
      <label for="desc">Description</label>
      <textarea id="desc" rows="4" placeholder="What happened and when?"></textarea>
      <button class="btn" type="button">Send report</button>
    </section>
  </main>
</template>