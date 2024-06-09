<script>
    export let experiences = [];
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Work Experience</h2>
    {#each experiences as experience}
      <div class="mb-4">
        <h3 class="text-xl font-semibold">{experience.title}</h3>
        <p class="text-gray-600">{experience.company} - {experience.years}</p>
        <p>{experience.description}</p>
      </div>
    {/each}
  </section>

  