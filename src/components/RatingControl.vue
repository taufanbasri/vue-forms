<template>
    <ul>
        <li :class="{ active: activeOptions === 'poor'}"><button @click="activate('poor')" type="button">Poor</button></li>
        <li :class="{ active: activeOptions === 'average'}"><button @click="activate('average')" type="button">Average</button></li>
        <li :class="{ active: activeOptions === 'great'}"><button @click="activate('great')" type="button">Great</button></li>
    </ul>
</template>

<script>
export default {
    data() {
        return {
            activeOptions: null
        }
    },
    methods: {
        activate(opt) {
            this.activeOptions = opt
        }
    },
}
</script>

<style scoped>
.active{
    border-color: #a00078;
}

.active button {
    color: #a00078;
}

ul {
    list-style: none;
    margin: 0.5rem 0;
    padding: 0;
    display: flex;
}

li {
    padding: 0 1rem;
    border: 1px solid #ccc;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

button {
    font: inherit;
    border: none;
    background-color: transparent;
    cursor: pointer;
}
</style>