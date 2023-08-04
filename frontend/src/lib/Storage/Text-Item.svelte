<script lang="ts">
    import Tag from "./Tag.svelte";
    export let content: string = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
    export let title: string = "Text title..."
    export let tags: string[] = ["funread", "test", "loremegebhgbeigjneoigneogbubeigbgeubi"]
</script>

<div class="item">
    <div class="item-header">
        <h3 class="text-title">{ title }</h3>
    </div>
    <div class="item-body">
        <p class="text">{ content }</p>
    </div>
    <div class="item-footer">
        {#each tags as x}
            <Tag tagname="{x}"/>
        {/each}
    </div>
</div>

<style>
    .item {
        width: 400px;
        height: 200px;
        flex-shrink: 0;
        
        border-radius: 25px;
        border: 1px solid #0A0;
        background: #FFF;
    }

    .item-header {
        position: relative;
        
        width: 400px;
        height: 50px;
        flex-shrink: 0;

        border-radius: 25px 25px 0px 0px;
        background: #BFB;
    }

    .text-title {
        position: relative;
        left: 50px;
        margin: 0px;

        display: flex;
        width: 300px;
        height: 50px;
        flex-direction: column;
        justify-content: center;
        flex-shrink: 0;

        overflow: hidden;
        color: #000;
        text-overflow: ellipsis;
        font-family: Inter;
        font-size: 30px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;        
    }

    .text {
        position: relative;
        margin: 0px;
        

        display:inline-block;
        width: 350px;
        height: 100px;
        flex-direction: column;
        justify-content: center;
        flex-shrink: 0;

        overflow: scroll;
        scrollbar-width: none;
        color: #428442;
        text-overflow: ellipsis;
        white-space: normal;
        font-family: Inter;
        font-size: 20px;
        font-style: italic;
        font-weight: 400;
        line-height: normal;
        text-align: left;
        
    }
    .item-body {
        height: 100px;
        width: 400px;
        margin: 0;
    }

    .item-footer {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 400px;
        height: 50px;
        flex-shrink: 0;
        overflow: scroll;
        scrollbar-width: none;

        border-radius: 0px 0px 24px 24px;
        background: #428442;
    }
</style>