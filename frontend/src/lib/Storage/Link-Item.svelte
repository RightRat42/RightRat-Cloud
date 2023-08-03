<script lang="ts">
    import { getContext } from "svelte";
    import Tag from "./tag.svelte";
    // export let id = item.items[0].id
    export let title:string = "Link title...";
    export let url:string = "g.co";
    export let tags:string[] = ["cool", "test", "test4"];
</script>

<div class="item">
    <a href="https://{ url }">
    <div class="item-header">
        <h3 class="link-title">{ title }</h3>
    </div>
    <div class="item-body">
        <a class="link-url" href="https://{ url }">{ url }</a>
    </div>
    <div class="item-footer">
        {#each tags as x}
            <Tag tagname="{x}"/>
        {/each}
    </div>
    </a>
</div>

<style>
    .item {
        width: 400px;
        height: 150px;
        flex-shrink: 0;
        
        border-radius: 25px;
        border: 1px solid #00A;
        background: #FFF;
    }

    .item-header {
        position: relative;
        
        width: 400px;
        height: 50px;
        flex-shrink: 0;

        border-radius: 25px 25px 0px 0px;
        background: #BBF;
    }

    .link-title {
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

    .link-url {
        position: relative;
        margin-left: 25px;
        

        display: flex;
        width: 350px;
        height: 50px;
        flex-direction: column;
        justify-content: center;
        flex-shrink: 0;

        overflow: hidden;
        color: #424284;
        text-overflow: ellipsis;
        font-family: Inter;
        font-size: 20px;
        font-style: italic;
        font-weight: 400;
        line-height: normal;
        text-decoration-line: underline;
        text-align: left;
        
    }
    .item-body {
        height: 50px;
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
        background: #424284;
    }
</style>