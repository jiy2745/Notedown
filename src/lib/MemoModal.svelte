

<script lang="ts">
    export let title: string;
    export let text: string;
    export let isOpen: boolean;

    function closeMemoModal(): void {
        isOpen = false;
    }
</script>

{#if isOpen}
<div class="background" on:click={closeMemoModal}>
    <div class="memo-modal" on:click|stopPropagation>
        <textarea bind:value={title}></textarea>
        <textarea bind:value={text}></textarea>
    </div>
</div>
{/if}

<style>
    textarea {
        width: 90%;
        border: none;
        outline: none;
        resize: none;
        margin: 5px;
    }

    .background {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .memo-modal {
        width: 300px;
        height: 500px;
        background-color: white;
        border-radius: 10px;
    }
</style>
