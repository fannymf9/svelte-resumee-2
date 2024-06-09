<script>
    export let education = [];
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Education</h2>
    {#each education as edu}
      <div class="mb-4">
        <h3 class="text-xl font-semibold">{edu.school}</h3>
        <p class="text-gray-600">{edu.years}</p>
        <p>{edu.program}</p>
      </div>
    {/each}
  </section>

  