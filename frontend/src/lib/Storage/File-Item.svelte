<script lang="ts">
    import Tag from "./Tag.svelte";
    export let title:string = "File title...";
    export let content:string = "00000000-0000-0000-0000-000000000000";
    export let tags:string[] = ["nice", "picture", "testpic"];
        
</script>

<div class="item">
    <a href="../src/assets/img/{ content }" target="_blank">
    <div class="item-header">
        <h3 class="file-title">{ title }</h3>
    </div>
    <div class="item-body">
        <p class="file-link" >{ content }</p>
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
        border: 1px solid #A00;
        background: #FFF;
    }

    .item-header {
        position: relative;
        
        width: 400px;
        height: 50px;
        flex-shrink: 0;

        border-radius: 25px 25px 0px 0px;
        background: #FBB;
    }

    .file-title {
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

    .file-link {
        position: relative;
        margin: 0;
        margin-left: 25px;
        margin-right: 25px;
        

        display: flex;
        width: 350px;
        height: 50px;
        flex-direction: column;
        justify-content: center;
        flex-shrink: 0;

        overflow: hidden;
        color: #844242;
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

        border-radius: 0px 0px 25px 25px;
        background: #844242;
    }
</style>