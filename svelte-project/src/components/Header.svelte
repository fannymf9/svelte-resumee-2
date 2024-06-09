<script>
    export let name;
    export let email;
    export let phone;
    let darkMode = false;
  
    function toggleDarkMode() {
      darkMode = !darkMode;
      document.documentElement.classList.toggle('dark', darkMode);
    }
  </script>
  
  <header class="bg-gray-800 text-white p-4 flex justify-between items-center">
    <div>
      <h1 class="text-3xl">{name}</h1>
      <p class="text-xl">{email}</p>
      <p class="text-xl">{phone}</p>
    </div>
    <button on:click={toggleDarkMode} class="bg-gray-700 p-2 rounded">
      {darkMode ? 'Light Mode' : 'Dark Mode'}
    </button>
  </header>
  
  <style>
    :global(.dark) {
      --bg-color: #1a202c;
      --text-color: #cbd5e0;
    }
  
    :global(body.dark) {
      background-color: var(--bg-color);
      color: var(--text-color);
    }
  </style>

  

