<template>
    <li>{{ item }}</li>
</template>

<script lang="ts">
export default {
    props: {
        item: {
            type: String,
            default: 'hello'
        }
    }
}
</script>