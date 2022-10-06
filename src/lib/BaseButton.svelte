<script lang="ts">
  export let color: string | null = null;
  export let count: number | null = null;
</script>


<button
  class:bg-gray-200={!color}
  class:bg-green-200={green}
  class:bg-red-200={red}
>
  <slot />

  {#if count != null}
    <span class="count">{ count }</span>
  {/if}
</button>

<style>
  .bg-gray-200 {
    background: #e5e7eb;
  }

  .bg-green-200 {
    background: #bbf7d0;
  }

  .bg-red-200 {
    background: #fecaca;
  }

  .count {
    font-size: 0.8rem;
    margin-left: 0.5rem;
    background: white;
    border-radius: 1000vw;
    padding-left: 0.75rem;
    padding-right: 0.75rem;
  }
</style>