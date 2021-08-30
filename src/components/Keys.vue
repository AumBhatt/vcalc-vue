<template>
    <div
        id="all-keys"
        class="all-keys"
    >
        <button
            v-for="key in allKeys"
            :key="key.id"
            :class="[ key.keyType + key.keyValue]"
            @click="printKey(key)"
        >
            {{ key.keyValue }}
        </button>
    </div>
</template>

<script>
export default {
    name: "Keys",
    data() {
        return {
            allKeys: [
                {id: 0, keyValue: 0, keyType: "num"},
                {id: 1, keyValue: 1, keyType: "num"},
                {id: 2, keyValue: 2, keyType: "num"},
                {id: 3, keyValue: 3, keyType: "num"},
                {id: 4, keyValue: 4, keyType: "num"},
                {id: 5, keyValue: 5, keyType: "num"},
                {id: 6, keyValue: 6, keyType: "num"},
                {id: 7, keyValue: 7, keyType: "num"},
                {id: 8, keyValue: 8, keyType: "num"},
                {id: 9, keyValue: 9, keyType: "num"},
                {id: 10, keyValue: '.', keyType: "dec"},
            ]
        }
    },
    methods: {
        printKey(key) {
            console.log(key.keyValue, key.keyType)
        }
    }
}
</script>

<style>

.all-keys {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

.active {
}
</style>