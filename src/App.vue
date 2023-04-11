<template>
    <SettingsBlock/>
</template>

<script>
import SettingsBlock from "@/components/Settings.vue";

export default {
    name: 'App',
    components: {
        SettingsBlock
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

.mainBlock{
display: flex;

}
.infoImg {
    width: 16px;
    height: 16px;
}
.nameBlock{
    width: 200px;
}
.bodyBlock{
    width: 392px;
}
</style>
