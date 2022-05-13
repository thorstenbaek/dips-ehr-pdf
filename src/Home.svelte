<script>
    import { onMount } from "svelte";  
    import { fhir, resource } from './SmartOnFhirStore.js';        
</script>

{#if $resource}
    <iframe class="pdf-frame" title="PDF" src="{$resource.content[3].attachment.url}#toolbar=0"></iframe>
{:else}
    Loading PDF Document...
{/if}

<style>
    .pdf-frame {
        height: 100%;
        width: 100%;
    }
</style>
