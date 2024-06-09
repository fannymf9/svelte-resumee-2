<script>
    import Tabs from './Tabs.svelte';
    export let education = [];
  
    let tabs = education.map((school, index) => ({
      label: school.school,
      name: `tab-${index}`
    }));
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Education</h2>
    <Tabs {tabs}>
      {#each education as school, index}
        <div slot={`tab-${index}`}>
          <h3 class="text-xl font-semibold">{school.school}</h3>
          <p class="text-gray-600">{school.years}</p>
          <p>{school.program}</p>
        </div>
      {/each}
    </Tabs>
  </section>

  