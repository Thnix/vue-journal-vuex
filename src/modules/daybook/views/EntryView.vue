<template>
    <div>

        <div class="entry-title d-flex justify-content-between p-2">

            <div>
                <span class="text-succes fs-3 fw-bold"></span>
                <span class="mx-1 fs-3">July</span>
                <span class="mx-2 fs-4 fw-light">2021, thursday</span>
            </div>

            <div>
                <button class="btn btn-danger mx-2">
                    Delete
                    <i class="fa fa-trash-alt"></i>
                </button>

                <button class="btn btn-primary">
                    Upload photo
                    <i class="fa fa-upload"></i>
                </button>
            </div>

        </div>

        <hr>

        <div class="d-flex flex-column px-3 h-75">
            <textarea placeholder="What happened today?"></textarea>
        </div>

        <Fab 
            icon="fa-save"
        />

        <img 
            src="https://plus.unsplash.com/premium_photo-1673170101259-3b5fe7f4602b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=708&q=80" 
            alt="entry-picture"
            class="img-thumbnail"
        >

    </div>

</template>

<script>
    import { defineAsyncComponent } from 'vue'

    export default {
        components: {
            Fab: defineAsyncComponent( () => import( "../components/FloatingButton.vue" ) )
        }
    }
</script>

<style lang="scss" scoped>
    textarea {
        border: none;
        font-size: 20px;
        height: 100%;

        &:focus {
            outline: none;
        }
    }
    img {
        bottom: 150px;
        box-shadow: 0px 5px 10px rgba( $color: #000000, $alpha: 0.2 );
        position: fixed;
        right: 20px;
        width: 200px;
    }
</style>