<template>
    <h1>Hello, {{ name }}</h1>
    <ul v-for="(item, index) in frameworks" :key="index">
        <li>{{ item }}</li>
    </ul>
</template>

<script setup>
defineProps({
    name : String,
        frameworks : Array,
})
</script>

<!--
<script>
export default {
    props : {
        name : String,
    }
}
</script>
-->
