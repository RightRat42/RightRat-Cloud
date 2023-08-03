<script lang="ts">
    import LinkItem from './lib/Storage/Link-Item.svelte';
    import Tag from './lib/Storage/tag.svelte';
    import TextItem from './lib/Storage/Text-Item.svelte';


    let module: string = "LinkItem";
</script>

<main>
  <h2>View Module: { module }</h2>

  <div class="card">
    <LinkItem />
  </div>
</main>

