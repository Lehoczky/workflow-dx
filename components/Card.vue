<template>
    <div style="border: 1px solid grey; border-radius: 4px;padding:16px 30px; display:grid;place-content:center;">
        <slot />
        <span style="margin-top: 8px;">{{ text }}</span>
    </div>
</template>

<script setup>
defineProps({
    text: {
        type: String,
        default: ""
    }
})
</script>