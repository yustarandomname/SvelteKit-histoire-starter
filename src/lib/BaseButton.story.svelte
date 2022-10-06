<script lang="ts">
  import type { Hst } from '@histoire/plugin-svelte'

  import BaseButton from "./BaseButton.svelte"

  export let Hst: Hst

  let text = "Click me"
</script>

<Hst.Story>
  <BaseButton>
    { text }
  </BaseButton>
</Hst.Story>