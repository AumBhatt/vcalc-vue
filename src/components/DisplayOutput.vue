<template>
    <div class="displayOutput">
        <div class="historyOutput">
            <span v-for="hist in this.$parent.historyList" :key="hist.id">{{ hist.exp }}</span>
        </div>
        <span class="currentOutput">
            {{ this.$parent.currentExp }}
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
    align-items: center;
    justify-content: flex-end;

}

.historyOutput {
    width: 100%;
    /* height: 75%; */
    max-height: 75%;

    display: flex;
    flex-direction: column;
    align-items: flex-end;
    justify-content: space-between;

    overflow-y: auto;
    scrollbar-width: none;

    font-size: 1.5em;
    font-weight: thin;


}

.historyOutput > span {
    margin: 2px;
}

.historyOutput::-webkit-scrollbar {
    width: 0px;
}

.currentOutput {
    width: 100%;
    height: 1.5em;

    border-bottom: 1px solid #fff4;

    font-size: 3.5em;
    text-align: right;

}
</style>