<script>
    export let tabs = [];
    export let selectedTab = 0;
  
    function selectTab(index) {
      selectedTab = index;
    }
  </script>
  
  <div class="tabs">
    {#each tabs as tab, index}
      <button on:click={() => selectTab(index)} class:active={selectedTab === index}>
        {tab.label}
      </button>
    {/each}
  </div>
  
  <div class="tab-content">
    {#if tabs[selectedTab]}
      <slot name={tabs[selectedTab].name} />
    {/if}
  </div>
  
  <style>
    .tabs {
      display: flex;
      gap: 1rem;
    }
    .tabs button.active {
      font-weight: bold;
    }
  </style>

  