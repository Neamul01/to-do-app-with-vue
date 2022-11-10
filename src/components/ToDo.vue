<template>
    <li>{{ item }}
        <button class="border-2 p-1 px-3" @click="removeThisTodo">Remove</button>
    </li>
</template>

<script lang="ts">
export default {
    props: {
        item: {
            type: String,
            default: ' '
        }
    },
    methods: {
        removeThisTodo() {
            this.$emit('removeThisTodo', this.item)
        }
    }
}
</script>