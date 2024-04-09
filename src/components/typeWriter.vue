<template>
    <p>{{ showText }}</p>
</template>

<script setup>
    import { ref } from 'vue'
    import { toRef } from 'vue'
    const SLEEP_TIME = 90

    const props = defineProps({
        text: String,
    })

    let showText = ref("")
    const propsText = toRef(props, "text")
    const strLen = propsText.value.length

    for(let i = 0; i < strLen; i++){
        setTimeout(() => {
            showText.value += propsText.value.substring(i, i + 1)
        }, SLEEP_TIME * i);
    }

    
</script>
