<script lang="ts">
  import LinkItem from './lib/Storage/Link-Item.svelte';
  import Tag from './lib/Storage/tag.svelte';
  import TextItem from './lib/Storage/Text-Item.svelte';
  import data from "./assets/data.json";

  let testtags = data.items[0].tags;

  let module: string = "LinkItem";
</script>

<main>
  <h2>View Module: { module }</h2>

  <div class="card">
    <LinkItem title="{data.items[0].title}" url="{data.items[0].content}" tags={testtags}/>
  </div>
</main>

