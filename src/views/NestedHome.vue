<template>
    <div class="nested-home">nested home</div>
</template>

<script>
export default {
    name: 'NestedHome',
    components: {},
    mounted() {
        console.log('NestedHome mounted')
    },
    activated() {
        console.log('NestedHome activated')
    },
}
</script>
