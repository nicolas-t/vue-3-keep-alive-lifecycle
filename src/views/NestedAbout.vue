<template>
    <div class="nested-about">nested about</div>
</template>

<script>
export default {
    name: 'NestedAbout',
    components: {},
    mounted() {
        console.log('NestedAbout mounted')
    },
    activated() {
        console.log('NestedAbout activated')
    },
}
</script>
