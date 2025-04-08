<script lang="ts">
    import MemoModal from "$lib/MemoModal.svelte";

    let title: string = "Memo title";
    let text: string = "Memo text";
    let isOpen: boolean = false;
</script>

<div class="memo" on:click={() => isOpen = true}>
    <p>{title}</p>
    <p>{text}</p>
</div>

<MemoModal
    bind:title
    bind:text
    bind:isOpen
/>

<style>
    .memo {
        width: 100px;
        height: 100px;
        background-color: wheat;
    }
</style>