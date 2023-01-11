<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContents.vue';

export default {
    components: {
        AppHeader,
        AppContent
    }
}
</script>

<template>
    <div>
        <AppHeader></AppHeader>
        <AppContent></AppContent>
    </div>
</template>

<style lang="scss">
@use './styles/generals.scss' as *;
</style>
