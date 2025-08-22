<script>
  import { onMount } from 'svelte';
  
  let registrationContent = '';
  
  onMount(async () => {
    try {
      const response = await fetch('/registration.html');
      if (response.ok) {
        registrationContent = await response.text();
      }
    } catch (error) {
    }
  });
</script>

{#if registrationContent}
  <div class="registration-footer">
    {@html registrationContent}
  </div>
{/if}

<style>
  .registration-footer {
    margin-top: 2rem;
    padding: 1rem;
    text-align: center;
    color: #666;
    font-size: 0.875rem;
    border-top: 1px solid #e2e8f0;
  }
</style>
