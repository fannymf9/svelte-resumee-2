<script>
    export let languages = [];
    export let skills = [];
  </script>
  
  <section class="p-4">
    <h2 class="text-2xl mb-4">Languages and Other Skills</h2>
    <h3 class="text-xl font-semibold">Languages</h3>
    <ul>
      {#each languages as language}
        <li>{language}</li>
      {/each}
    </ul>
    <h3 class="text-xl font-semibold mt-4">IT Skills</h3>
    <ul>
      {#each skills as skill}
        <li>
          {skill}
          <div class="w-full bg-gray-200 rounded-full mt-1">
            <div class="bg-blue-600 text-xs font-medium text-blue-100 text-center p-0.5 leading-none rounded-full w-3/4">75%</div>
          </div>
        </li>
      {/each}
    </ul>
  </section>

  

