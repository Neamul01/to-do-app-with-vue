<template>
    <ul>
        <!-- @ts-ignore -->
        <ToDo v-for="item, index in todo" :key="index" :item="item" />
        <button class="border-2 p-1 px-3" @click="removelist">Empty List</button>
    </ul>
</template>

<script lang="ts">
import ToDo from './ToDo.vue'

export default {
    components: {
        ToDo
    },
    props: {
        todo: {
            type: Array,
            default: () => []
        }
    },
    methods: {
        removelist() {
            this.$emit('removelist')
        }
    }
}
</script>