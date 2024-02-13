<template>
    <div class="app-wrapper">
        <div class="container">
            <OtButton />
        </div>
        <div class="container">
            <OtList />
        </div>
    </div>
</template>

<script setup lang="ts">
import OtButton from "./components/OtButton.vue";
import OtList from "./components/OtList.vue";
import { ref } from "vue";

// TODO: implement name, seed_count and last_updated attribute
const list = ref([]);

// TODO: Fetch content from API when the button is clicked.
// TODO: Set the loading state of the button and forward the data to the list when ready.
// TODO: Make sure to append the new content, such that it doesn't override the existing content.
// TODO: Use this list to fetch the data from: https://openlibrary.org/people/george08/lists.json?limit=2&offset=0
function fetchContentAndAppendToList() {

}
</script>

<style scoped>
.app-wrapper {
    display: flex;
    align-items: center;
    font-size: 2rem;
}

.container {
    width: 500px;
}
</style>
