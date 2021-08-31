<template>
    <div
        id="all-keys"
        class="all-keys"
    >
        <button
            v-for="key in allKeys"
            :key="key.id"
            :class="[
                !isNaN(key.keyValue) ? `numKey` : key.keyName,
                (key.keyValue === 'backspace')?'material-icons-outlined':'calcKeys'
            ]"
            @click="keyPressed(key)"
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
                {id: 18, keyValue: "AC", keyName: "allClearKey"},
                {id: 17, keyValue: 'backspace', keyName: "backspaceKey"},
                {id: 16, keyValue: "%", keyName: "percentKey"},
                {id: 15, keyValue: "÷", keyName: "divKey"},
                {id: 7, keyValue: 7},
                {id: 8, keyValue: 8},
                {id: 9, keyValue: 9},
                {id: 14, keyValue: "x", keyName: "mulKey"},
                {id: 4, keyValue: 4},
                {id: 5, keyValue: 5},
                {id: 6, keyValue: 6},
                {id: 13, keyValue: "-", keyName: "subKey"},
                {id: 1, keyValue: 1},
                {id: 2, keyValue: 2},
                {id: 3, keyValue: 3},
                {id: 12, keyValue: "+", keyName: "addKey"},
                {id: 10, keyValue: '.', keyName: "decimalKey"},
                {id: 0, keyValue: 0},
                {id: 11, keyValue: '=', keyName: "equalKey"},
            ]
        }
    },
    methods: {
        keyPressed(key) {
            if(isNaN(key.keyValue)) {
                // not a number / its a function
            } else {
                // is a number / not a function
            }
        }
    }
}
</script>

<style>

.all-keys {
    width: 100%;
    height: 50%;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    
}

.all-keys > button {
    margin: 0.25em;

    border: none;

    color: #e67e22;
    font-size: x-large;
    background: none;
}

.all-keys > .material-icons-outlined {
    font-size: 1.5em;
}

.calcKeys {

    font-family: 'Comfortaa', cursive;

}

.all-keys > .numKey {
    color: white;
}

.all-keys > .equalKey {
    grid-column-start: 3;
    grid-column-end: 5;

    border-radius: 1em;

    color: white;
    background: #e67e22;
}
</style>