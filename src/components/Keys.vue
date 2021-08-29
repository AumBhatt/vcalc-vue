<template>
    <div id="function-keys"></div>
    <div
        id="num-keys"
        class="num-keys"
    >
        <button
            v-for="key in numKeys"
            :key="key"
            class="active"
            @click="printKey(key)"
        >
            {{ key }}
        </button>
    </div>
</template>

<script>
export default {
    name: "Keys",
    data() {
        return {
            numKeys: [
                {id: 0, }
            ]
        }
    },
    methods: {
        printKey(key) {
            console.log(key)
        }
    }
}
</script>

<style>

.num-keys {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

.active {
}
</style>