<template>
    <h1>Vue 3 keep-alive lifecycle</h1>

    <div class="instructions">
        <h3>Steps</h3>
        <div>1. Open devtools, console tab.</div>
        <div>2. Click <router-link :to="'/about/nested'">About link</router-link>.</div>
        <div>3. Clear console.</div>
        <div>4. Click <router-link :to="'/home/nested'">Home link</router-link>.</div>
        <h3>Observations</h3>
        <div><span class="code">activated</span> event is called on <span class="code">NestedAbout</span> component, even if we are deactivating it.</div>
        <div><span class="code">mounted</span> event is called twice on <span class="code">NestedHome</span> component.</div>
        <h3>Expected behaviour</h3>
        <div><span class="code">activated</span> event is not called on <span class="code">NestedAbout</span> component.</div>
        <div><span class="code">mounted</span> event is called only once on <span class="code">NestedHome</span> component.</div>
    </div>
    <div id="nav">
        <router-link to="/home/nested">Home</router-link> |
        <router-link to="/about/nested">About</router-link>
    </div>

    <router-view v-slot="{ Component }">
        <keep-alive>
            <component :is="Component" />
        </keep-alive>
    </router-view>
</template>

<script>
export default {
    components: {},
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    line-height: 1.5;
}
span.code {
    font-family: monospace;
    padding: 3px;
    background: #efefef;
}
.instructions {
    text-align: left;
    border-bottom: 1px solid silver;
    padding: 20px;
}

#nav {
    padding: 30px;
}

#nav a {
    font-weight: bold;
    color: #2c3e50;
}

#nav a.router-link-exact-active {
    color: #42b983;
}
</style>
