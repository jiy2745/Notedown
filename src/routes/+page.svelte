<script>
    let isMemoClicked = false;
    function memoClick() {
        isMemoClicked = true;
    }
</script>

<div class="memo" on:click={memoClick} class:is-memo-clicked={isMemoClicked}></div>

<style>
    .memo {
        width: 100px;
        height: 100px;
        background-color: wheat;
    }

    .is-memo-clicked {
        background-color: blueviolet;
    }
</style>