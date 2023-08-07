<script lang="ts">
    import data from "../../../../backend/src/assets/data.json";
    import FileItem from "./File-Item.svelte";
    import LinkItem from "./Link-Item.svelte";
    import TextItem from "./Text-Item.svelte";
    let items = data.items
</script>

<body>
    <header>
        <h1>RightRat's Cloud</h1>
    </header>
    <div class="addDiv">
        <button class="add">
            + Add
        </button>
    </div>
    <div class="storage">
        {#each items as x}
            {#if x.type=="link"}
                <LinkItem title="{ x.title }" content="{ x.content }" tags={x.tags}/>
            {:else if x.type=="text"}
                <TextItem title="{ x.title }" content="{ x.content }" tags={x.tags}/>
            {:else if x.type=="file"}
                <FileItem title="{ x.title }" content="{ x.content }" tags={x.tags}/>
            {/if}
        {/each}
    </div>
</body>

<style>
    header {
        min-width: 450px;
        display: flex;
        flex: 7;
        top: 0;
        width: 100vw;
        flex-shrink: 0;
        align-content: start;
        justify-content: center;

        border-radius: 25px;
        border: 2px solid #000;
        box-sizing: border-box;
        background: #BBB;
        box-shadow: 0px 50px 50px 0px rgba(255, 0, 0, 0.25);
    }

    body {
        display: flex;
        align-content: start;
        flex-direction: column;
    }

    h1 {
        margin: 0px;
        display: flex;
        width: 480px;
        height: inherit;
        flex-direction: column;
        justify-content: center;
        flex-shrink: 0;

        color: #000;
        text-align: center;
        font-family: Inter;
        line-height: normal;
        font-size: min(9vw, 50px);
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }

    .addDiv {
        display: flex;
        align-items: center;
        justify-content: center;
        flex: 1;
        flex-shrink: 0;
        width: 100vw;
        flex-shrink: 0;
        min-width: 450px;
        border-radius: 25px;
        border: 2px  solid #000;
        border-top: 0;
        border-bottom: 0;
        box-sizing: border-box;
        background: #DDD;
        
    }

    .add {
        display: block;
        margin: 0;
        padding: 0;
        width: 10vw;
    }

    .storage {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        flex: 90;
        width: 100vw;
        flex-shrink: 0;
        min-width: 450px;
        justify-content: space-evenly;
        align-items:center;

        border-radius: 25px;
        border: 2px solid #000;
        box-sizing: border-box;
        background: #FFF;
    }
</style>