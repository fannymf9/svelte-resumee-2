<script>
    export let schools = [];
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Education</h2>
    {#each schools as school}
      <div class="mb-4">
        <h3 class="text-xl font-semibold">{school.degree}</h3>
        <p class="text-gray-600">{school.school} - {school.years}</p>
        <p>{school.description}</p>
      </div>
    {/each}
  </section>

  