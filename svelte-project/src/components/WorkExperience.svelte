<script>
    export let jobs = [];
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Experience</h2>
    {#each jobs as job}
      <div class="mb-4">
        <h3 class="text-xl font-semibold">{job.title}</h3>
        <p class="text-gray-600">{job.company} - {job.years}</p>
        <p>{job.description}</p>
      </div>
    {/each}
  </section>

  