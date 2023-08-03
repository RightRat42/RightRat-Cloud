<script lang="ts">
    let title:string = "Link title..."
    let url:string = "Link url..."
    let tags:string[] = []
</script>

<div class="link-item">
    <div class="link-item-header">
        <h3 class="link-title">{ title }</h3>
    </div>
    <div class="link-item-body">
        <p class="link-url">{ url }</p>
    </div>
    <div class="link-item-footer">

    </div>
</div>

<style>
    .link-item {
        width: 400px;
        height: 150px;
        flex-shrink: 0;
        
        border-radius: 25px;
        border: 1px solid #00A;
        background: #FFF;
    }

    .link-item-header {
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
        left: 25px;
        margin: 0px;
        

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
    .link-item-body {
        height: 50px;
        width: 400px;
        margin: 0;
    }

    .link-item-footer {
        width: 400px;
        height: 50px;
        flex-shrink: 0;

        border-radius: 0px 0px 24px 24px;
        background: #424284;
    }
</style>