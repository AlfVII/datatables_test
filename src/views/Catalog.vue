<script setup>

import Catalog from '/src/components/Catalog.vue'

</script>

<script>
export default {
    data() {
        const currentCatalog = "/catalog.ndjson"
        return {
            currentCatalog,
        }
    },
    methods: {
    },
    mounted() {
    },
    created() {
    },
}
</script>

<template>
    <div class="d-flex flex-column min-vh-100">
        <main role="main" class="main p-0 m-0">
            <Catalog
                class="container content pt-2"
                :catalogInput="currentCatalog"
                :name="'Test Catalog'"
                :dataTestLabel="'Catalog'"
            />
        </main>
    </div>
</template>

<style>
    .wrap {
      position: relative;
    }

    .wrap:before {
      content: ' ';
      display: block;
      position: absolute;
      width: 100%;
      height: 100%;
      opacity: 1;
      background-image: linear-gradient(to bottom, rgba(26, 26, 26, 0.8), rgba(26, 26, 26, 1)),
    url('/images/background_home.png');
      background-repeat: no-repeat;
      background-position: 50% 0;
      background-size: cover;
    }

    .content {
      position: relative;
    }
</style>