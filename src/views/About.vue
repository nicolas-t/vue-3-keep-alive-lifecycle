<template>
    <div class="about">
        <h1>This is an about page</h1>
        <RouterView />
    </div>
</template>
<script>
export default {
    name: 'About',
    components: {},
    mounted() {
        console.log('About mounted')
    },
    activated() {
        console.log('About activated')
    },
}
</script>
