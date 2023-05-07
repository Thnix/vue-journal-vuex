<template>
  <div>
    <div class="d-flex justify-content-center">
        <h1 class="align-self-center">Nothing selected</h1>
    </div>

    <Fab />
  </div>
</template>

<script>
    import { defineAsyncComponent } from 'vue';

    export default {
        components: {
            Fab: defineAsyncComponent( () => import( "../components/FloatingButton.vue" ) )
        }
    }
</script>

<style lang="scss" scoped>
    div {
        height: 100%;
    }
</style>