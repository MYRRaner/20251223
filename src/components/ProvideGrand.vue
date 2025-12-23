<template>
    <div>爷爷组件--提供资金{{ money }}</div>
    <hr>
    <ProvideParent />
</template>

<script setup>
    import ProvideParent from './ProvideParent.vue'
    import { ref, provide } from 'vue'
    const money = ref(1000)
    const updateMoney = (value)=>{ money.value += value}
    provide('money', money)
    provide('updateMoney', updateMoney)
</script>