<template>
    <ul>
        @ts-ignore
        <ToDo v-for="item, index in todo" :key="index" :item="item" />
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
    }
}
</script>