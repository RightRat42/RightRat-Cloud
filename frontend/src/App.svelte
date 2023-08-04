<script lang="ts">
  import LinkItem from './lib/Storage/Link-Item.svelte';
  import Tag from './lib/Storage/Tag.svelte';
  import TextItem from './lib/Storage/Text-Item.svelte';
  import data from "./assets/data.json";
  import files from "./assets/files.json"
  import FileItem from './lib/Storage/File-Item.svelte';
  import {v4 as uuid} from "uuid"
    import Storage from './lib/Storage/Storage.svelte';
  // const uuidRegExp = /^[0-9a-fA-F]{8}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{12}$/gi;
  // const index: number = 2;
  // let linktags = data.items[index].tags;
  // let module: string = "FileItem";
  
  
  
  
</script>

<main>
  <!-- <h2>View Module: { module }</h2> -->

  <!-- <div class="card">
    <FileItem title="{ data.items[index].title }" content="{ passUuid }" tags={ linktags }/>
  </div> -->

  <Storage />
</main>

