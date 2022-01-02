<template>
    <div class="home">
        <h1>This is an home page</h1>
        <RouterView />
    </div>
</template>

<script>
export default {
    name: 'Home',
    components: {},
    mounted() {
        console.log('Home mounted')
    },
    activated() {
        console.log('Home activated')
    },
}
</script>
