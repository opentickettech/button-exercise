<template>
    <div class="list">
        <div class="list__header">
            This is a list of books:
        </div>
        <div class="list__content">
            <!-- TODO: implement loop for displaying the items of the list property -->
<!--            <div class="list__item">-->
<!--                <div class="list__item__name"></div>-->
<!--                <div class="list__item__seed_count"></div>-->
<!--                <div class="list__item__last_updated"></div>-->
<!--            </div>-->
        </div>
    </div>
</template>

<script setup lang="ts">
import { ListItem } from "../types.ts";

type Props = {
    list?: ListItem[],
}

defineProps<Props>();

</script>

<style lang="scss" scoped>
.list {
    &__header {
        margin-bottom: 2rem;
    }

    &__item {
        background-color: #213547;
        color: white;
        border-radius: 0.5rem;
        font-size: 1.2rem;
        margin: 0.5rem;
        text-align: left;
        padding: 0.5rem 1rem;

        &__seed_count, &__last_updated {
            font-size: 1rem;
        }
    }
}
</style>
