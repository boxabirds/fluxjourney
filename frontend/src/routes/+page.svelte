<script>
    import TopNav from '$lib/components/TopNav.svelte';
    import MainPanel from '$lib/components/MainPanel.svelte';
    import ImagineBar from '$lib/components/ImagineBar.svelte';
    import BottomNav from '$lib/components/BottomNav.svelte';
  
    let innerWidth; // Declare the variable to bind to window.innerWidth
  </script>
  
  <style>
    /* Add your CSS for layout here */
    @media (max-width: 636px) {
      /* Mobile-specific styles */
    }
  
    @media (min-width: 637px) {
      /* Desktop-specific styles */
    }
  </style>
  
  <TopNav />
  <MainPanel />
  
  <!-- Bind innerWidth to window.innerWidth -->
  <svelte:window bind:innerWidth />
  
  {#if innerWidth > 636}
    <!-- Desktop specific components -->
  {/if}
  
  <ImagineBar />
  <BottomNav />
  