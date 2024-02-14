<template>
    <div class="button-wrapper">
        <button type="button">{{ message }}</button>
    </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

type Props = {
    disabled?: boolean,
    loading?: boolean,
}

defineProps<Props>();

// TODO: propagate the click event to the app wrapper
// TODO: add a loading state with a spinning icon by changing the class of the button to .is-loading and removing the text.
const message = computed(() => {
    return "Fetch list";
})

</script>

<style scoped lang="scss">
.button-wrapper {
    & button{
        min-width: 15rem;
        min-height: 5rem;
        position: relative;

        &.loading:after {
            animation: spinAround 1s infinite linear;
            font-family: "OpenTicketIcons" !important;
            content: "\f145";
            display: block;
            position: absolute;
            width: 3rem;
            height: 2rem;
            top: calc(50% - 1rem);
            left: calc(50% - 1.5rem);
        }

        &.disabled {
            cursor: not-allowed;
            opacity: 0.7;
            color: grey;
            pointer-events: none;
        }
    }
}
</style>
