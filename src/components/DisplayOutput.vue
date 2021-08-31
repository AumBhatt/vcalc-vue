<template>
    <div class="displayOutput">
        <div class="historyOutput">
            <span v-for="hist in this.$parent.historyList" :key="hist.id">{{ hist.exp }}</span>
        </div>
        <span class="currentOutput">
            {{ (exp = this.$parent.currentExp)?exp:"a" }}
        </span>
    </div>
</template>

<script>
export default {
    name: "Display"
}
</script>

<style>
.displayOutput {
    width: 100%;
    height: 50%;

    display: flex;
    flex-direction: column;
    justify-content: flex-end;

    background: red;
}

.historyOutput {
    width: 100%;
    /* height: 75%; */

    display: flex;
    flex-direction: column;
    align-items: flex-end;
    justify-content: space-between;

    /* padding-top: 1.25em; */

    overflow-y: auto;
    scrollbar-width: none;

    font-size: 1.25em;

    background: blue;

}

.historyOutput::-webkit-scrollbar {
    width: 0px;
}

.currentOutput {
    width: 100%;
    height: auto;

    font-size: 2.5em;
    text-align: right;

    background: grey;
}
</style>