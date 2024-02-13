<template>
    <div class="list">
        <div class="list__header">
            This is a list of books:
        </div>
        <div class="list__content">        
            <!-- TODO: implement loop for displaying the items of the list property -->
           <div class="list__item">
                <div class="list__item__name">Name</div>
                <div class="list__item__seed_count">2</div>
                <div class="list__item__last_updated">20-02-2024</div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
defineProps(['list']);

</script>

<style lang="scss" scoped>
.list {
    &__header {
        margin-bottom: 2rem;
    }

    &__item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #213547;
        color: white;
        border-radius: 0.5rem;
        font-size: 1.2rem;
        margin: 0.5rem;
        padding: 0.5rem 1rem;

        &__seed_count, &__last_updated {
            font-size: 1rem;
        }
    }
}
</style>
