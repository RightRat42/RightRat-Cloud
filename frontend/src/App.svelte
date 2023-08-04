<script lang="ts">
  import LinkItem from './lib/Storage/Link-Item.svelte';
  import Tag from './lib/Storage/Tag.svelte';
  import TextItem from './lib/Storage/Text-Item.svelte';
  import data from "./assets/data.json";
  import FileItem from './lib/Storage/File-Item.svelte';

  const index: number = 2;
  let linktags = data.items[index].tags;
  let module: string = "FileItem";
</script>

<main>
  <h2>View Module: { module }</h2>

  <div class="card">
    <FileItem title="{data.items[index].title}" content="{data.items[index].content}" tags={ linktags }/>
  </div>
</main>

