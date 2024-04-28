<template>
    <div class="blacklabel">
        <h1>{{ props.text }}</h1>
    </div>
</template>

<script setup>
    const props = defineProps({
        text: String
    })
</script>

<style>
    .blacklabel{
        margin: 16px;
        background-color: #201919;
    }
</style>