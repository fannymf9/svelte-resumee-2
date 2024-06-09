<script>
    import Tabs from './Tabs.svelte';
    export let jobs = [];
  
    let tabs = jobs.map((job, index) => ({
      label: job.company,
      name: `tab-${index}`
    }));
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Work Experience</h2>
    <Tabs {tabs}>
      {#each jobs as job, index}
        <div slot={`tab-${index}`}>
          <h3 class="text-xl font-semibold">{job.title}</h3>
          <p class="text-gray-600">{job.company} - {job.years}</p>
          <ul class="list-disc list-inside">
            {#each job.tasks as task}
              <li>{task}</li>
            {/each}
          </ul>
        </div>
      {/each}
    </Tabs>
  </section>
  

